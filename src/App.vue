<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <code-input
    @complete="completed = true"
    :fields="3"
    :fieldWidth="56"
    :fieldHeight="56"
    :required="true"
  />
  <button class="btn" :disabled="!completed">Continue</button>
</template>

<script setup>
import CodeInput from "./components/CodeInput.vue";
import { ref } from "vue";

const completed = ref(false);
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn {
  margin-top: 10px;
  border-radius: 8px;
  font-size: 20px;
  border: 0;
  color: #fff;
  background-color: #398ee2;
  cursor: pointer;
  padding: 8px 16px;
  transition: 0.2s all ease-in-out;
}
.btn:disabled {
  background-color: #76b8fa;
}
</style>
