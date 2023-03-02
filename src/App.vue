<script>
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
      if(this.contador > 0){
        this.contador--
      }
    },
    reset() {
      this.contador = 0
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}
</script>

<template>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <button @click="reset">Resetar</button>
 <div class="contador">  {{ contador }} </div>
</template>

<style scoped>
button {
  background-color: white;
  color: aqua;
  border: 1px solid black;
  font-weight: 50px;
  display: flex;
  justify-content: center;
  align-items: center;

}
button:hover{
  background-color: black;
  color: blue;
}
.contador{
  border: 1px solid black;
  font-weight: 50px
  ;
}
</style>
