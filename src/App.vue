<template>
  <div id="app">

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      characterData: null
    }
  },
  mounted() {
    this.getCharacters();
},
methods: {
  getCharacters: function(){
    fetch("https://rickandmortyapi.com/api/character")
    .then(response => response.json())
    .then(data => console.log(data));
  }
}
}

</script>
