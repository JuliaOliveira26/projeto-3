<script setup>
import { ref } from 'vue'

const contador = ref(10)

function incrementar() {
  contador.value++
  console.log(contador)
}
</script>

<template>
  <div>
    contador: {{ contador }}
  </div>
    <button @click="incrementar">+</button>
    <button @click="$event => contador --">-</button>
    <button @click="mostrarDiv = !mostrarDiv">Alternar </button>

    <div v-if="mostrarDiv"> Vou mostrar o conteudo... </div>
</template>
<style></style>