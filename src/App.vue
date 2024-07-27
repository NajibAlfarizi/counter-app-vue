// composition api

<script setup>
import { ref } from "vue";
const count = ref(0);

function increment() {
  count.value++;
}

function decrement() {
  count.value--;
}
</script>

<template>
  <main>
    <div>
      <h1>Counter App</h1>
      <span id="value">{{ count }}</span>
      <div>
        <button @click="decrement" id="decrement">-</button>
        <button @click="increment" id="increment">+</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  text-align: center;
  background-color: #333333;
  padding: 20px;
  border-radius: 10px;
}

#value {
  font-size: 5rem;
  font-weight: normal;
  margin: 0;
}

button {
  font-size: 16px;
  margin: 0 5px;
  background-color: #555555;
  color: #ffffff;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

button:hover {
  background-color: #777777;
}

button:active {
  animation: pulse 0.5s linear;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}
</style>
