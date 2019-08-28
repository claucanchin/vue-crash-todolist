<template>
  <div>
    <div v-for="eachtodo in todos" v-bind:key="eachtodo.id">
      <TodoItem v-bind:todo="eachtodo" v-on:del-todo="$emit('del-todo', eachtodo.id)" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem.vue";

export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ["todos"]
};
</script>

<style scoped>
</style>