<script setup>
const nome = 'manu'
const idade = 16

 function inverter(texto) {
  return texto.split('').reverse().join('')
 }
 function saudacao() {
  return `Olá, ${nome}`

 }
 import { ref } from 'vue'

const contador = ref(0)

function decrementar () {
  contador.value--
}
</script>]
<template>
  <div class="info">
      <p>Nome: {{ nome }} </p>
      <p>Idade: {{ idade }}  anos</p>
      <hr />
      <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
      <p>O nome tem {{ nome.length }}  caracteres</p>
      <p>O nome invertido é: {{ inverter(nome.toUpperCase()) }} </p>
      <hr />
      <p> Exemplo de saudação usando função</p>
      <p> {{ saudacao() }}  </p>
    <button @click="contador++">+</button>
    <button @click="decrementar">-</button>
    <p>valor do contador: {{ contador }}</p>
    <div v-if = "contador > 10" class="verde" > <p>Contador maior que 10</p></div>
    <div v-else class="vermelho" > <p>Contador menor que 10</p></div>
  </div>

</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Madimi+One&display=swap');

.info {
font-family: "Madimi One", sans-serif;
background-color: rgb(0, 0, 0);
padding: 20px 30px;
color: rgb(183, 210, 219);
border-radius: 10px;
}
.vermelho {
  color: red;
}
.verde {
  color: green;
}
h1 {
color: white;
font-weight: bold;
font-size: 1.5em;
}
</style>