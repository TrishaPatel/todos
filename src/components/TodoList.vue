<template>
  <div class="md-layout  md-alignment-center">
    <div class="md-layout-item md-size-40">
      <h1>To-do List</h1>
      <md-content>
        <ul>
          <li v-for="(todo, index) in todos" :key="index">
            {{ todo.description }}
          </li>
        </ul>
      </md-content>
    </div>
  </div>
</template>

<script>
export default {
  name: "TodoList",
  data() {
    return {
      todos: [
        { description: "Difference between Vue and React", completed: false },
        { description: "Naming Conventions in Vue.js", completed: false },
        { description: "Learn Vue.js", completed: false }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  text-align: left;
  padding: 10px;
}
a {
  color: #42b983;
}
</style>
