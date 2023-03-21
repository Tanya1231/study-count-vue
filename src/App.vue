<template>
  <div id="app">
  <h1>Methods</h1>
  <p>Count {{ number }}</p>
  <button @click="increaseHandler">increase count</button>
  <button @click="reduceHandler">reduce count</button>
</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      number: 0
    };
  },
  methods: {
    increaseHandler() {
      this.number++;
    },
    reduceHandler(){
      this.number--;
      if(this.number < 0) {
        this.number = 0;
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
