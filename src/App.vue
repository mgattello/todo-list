<template>
  <div id="app">
    <List :todos="todos"/>
  </div>
</template>

<script>
import List from './components/List.vue';

export default {
  name: 'app',
  components: {
    List
  },
  data () {
    return {
      todos: [
        {
          id: 1,
          title: "Todo sdsdas",
          completed: false
        },
        {
          id: 2,
          title: "Todo 11sdsdas",
          completed: false
        },
        {
          id: 3,
          title: "Todo sdss11daddas",
          completed: false
        },
        {
          id: 4,
          title: "Todo sdsdasddadasdas",
          completed: false
        }
      ]
    }
  },
  methods: {
    delete(id) {
      this.todos = this.todos.filter(todo => todo.id !== id );
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
