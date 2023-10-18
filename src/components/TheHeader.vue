<template>
  
  <h1 :class="{ 'title': true, 'title-home': isHome }">
    Curso Vue 3
  </h1>

  <p>
    
  </p>
  
  
  <div 
    v-for="(obj, index) in todos"
    :key="obj.id"
    class="todos-item"
  >
    <img 
      v-if="obj.imgSrc"
      :src="obj.imgSrc"
    />
    
    {{ index }} - {{ obj.title }}
    
  </div>
  
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isHome: false,
      classVar: 'title',
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSrc": "https://via.placeholder.com/150"
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}

.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;
  border-radius: 4px;
}

.title-home {
  font-size: 40px;
  color: greenyellow;
}

.title {
  font-size: 20px;
  color: blue;
}
</style>