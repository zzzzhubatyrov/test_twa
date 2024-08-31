<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import WebApp from '@twa-dev/sdk'

import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src={viteLogo} class="logo" alt="Vite logo" />
    </a>
    <a href="https://react.dev" target="_blank">
      <img src={reactLogo} class="logo react" alt="React logo" />
    </a>
  </div>
  <h1>Vite + React</h1>
  <div class="card">
    <button @click="count.value++">
      count is {{ count }}
    </button>
  </div>
  {/* Here we add our button with alert callback */}
  <div class="card">
    <button @click="WebApp.showAlert(Hello World! Current count is ${count.value})">
      Show Alert
    </button>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
