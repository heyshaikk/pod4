<template>
  <div>
    <h1>Dynamic Component Loading - Vue.js</h1>
    <lazyLoad />
    <button @click="loginIn">Load Ad</button>
    <div v-if="showComponent">
      <loginIn />
    </div>
  </div>
</template>

<script>

import loginIn from "./components/loginIn.vue";
import lazyLoad from "./components/lazyLoad.vue";

export default {
  name: "App",
  components: {
    loginIn,
    lazyLoad,
  },
  data() {
    return {
      showComponent: false,
    };
  },
  methods: {
    loginIn() {
      this.showComponent = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
button {
  padding: 10px;
  border-color: black;
  border-radius: 15px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
* {
  color: black;
  font-family: "Times New Roman", Times, serif;
}
</style>
