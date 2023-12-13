<template>
  <div class="container">
    <img src="./assets/logo.svg"  alt="logoVue" width="125" height="125"/>
    <small>
      <h1>Hola</h1>
    </small>  
  </div>
  <div class="container">
     <h2>Contador: {{ count }}</h2>
     <button @click="incrementCount()" class="button">+</button>
     <button @click="decreaseCount()"  class="button">-</button>
     <button @click="resetCount()" class="button">Reset</button>
  </div>
</template>

<script>
export default {
  data : () => ({
    count : 0,
  }),
  methods:{
    incrementCount () {
      this.count++
    },
    decreaseCount () {
      this.count-- 
    },
    resetCount () {
      this.count = 0
    } 
  }
  }
</script>

<style scoped>
 .container {
   text-align: center;
   color: aliceblue;
 }

  h1 {
    font-weight: bolder;
  }
  h2 {
    font-size: 2.5rem;
  }
  .button {
    background-color: #7c7c7c;
    border-style: none;
    color: #2e2e2e;
    cursor: pointer;
    font-size: 1.5rem;
    margin: 0 4px;
    border-radius: 8px;
  }
  .button:hover {
    color: #000000;
    background-color: #e7e7e7;
  }
</style>