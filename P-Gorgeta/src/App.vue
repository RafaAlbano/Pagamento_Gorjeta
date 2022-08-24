<script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
  <main>
    <div class="input">
      <h2>Calculadora de Gorjetas</h2>
      <h3>Valor da Conta</h3>
      <input type="number" v-model="valor1" placeholder="Valor da conta" />

      <h3>Quantidade de desconto</h3>
      <select name="Qualidade de serviço" id="asd" v-model="gorgeta">
        <option value="5">5%</option>
        <option value="10">10%</option>
        <option value="15">15%</option>
        <option value="20">20%</option>
        <option value="25">25%</option>
      </select>

      <h3>Quantidade de amigos</h3>
      <input
        type="number"
        placeholder="quantidade de amigos"
        v-model="valor2"
      />

      <p class="pagamento">
        Valor para cada um pagar: {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}
      </p>
    </div>
  </main>
</template>
<style>
.input {
  flex-direction: column;
  display: flex;
  justify-content: center;
}
h3 {
  font-family: "Times New Roman", Times, serif;
  color: black;
}
h2 {
  font-family: "Times New Roman", Times, serif;
}
select {
  display: block;
  width: 100%;
  height: 25px;
  margin-bottom: 10px;
  border: 1px solid white;
  border-radius: 10px;
}
main {
  background-color: aliceblue;
  padding: 30px;
  margin: 10% auto;
  border-radius: 15px;
  height: 500px;
  margin-left: 13%;
  width: 900px;
}
input {
  display: block;
  width: 100%;
  height: 25px;
  margin-bottom: 10px;
  border: 1px solid black;
  border-radius: 5px;
}
.pagamento {
  color: red;
}
</style>
