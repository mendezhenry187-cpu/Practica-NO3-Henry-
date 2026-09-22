<script setup lang="ts">
import { ref } from 'vue'

// Variable reactiva para el contador
const contador = ref<number>(0)

// Funciones para aumentar y disminuir
const incrementar = () => {
  contador.value++
}

const decrementar = () => {
  contador.value--
}
</script>

<template>
  <main style="text-align: center; margin-top: 50px; font-family: sans-serif;">
    <h1>Práctica No. 3 - Contador</h1>
    <p>Valor actual:</p>
    <h2 style="font-size: 48px;">{{ contador }}</h2>
    
    <div style="margin-top: 20px;">
      <button @click="decrementar" style="padding: 10px 20px; font-size: 18px; margin-right: 10px; cursor: pointer;">- Disminuir</button>
      <button @click="incrementar" style="padding: 10px 20px; font-size: 18px; cursor: pointer;">+ Aumentar</button>
    </div>
  </main>
</template>