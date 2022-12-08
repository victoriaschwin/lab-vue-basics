<script setup>
import Nav from "./components/Nav.vue";
import Footer from "./components/Footer.vue";
import { ref } from "vue";

let name = ref('Ariadna');
const show = ref("show")

function changeName(){
  
 return name = "Victoria"
}

function changeShow(){
  if(show.value === "show"){
    show.value = "hidden";
  }else{
    show.value = "show"
  }
}
</script>

<template>
  <div>
    <Nav />
    <div>
      <p>{{(2+2)}}</p>
      <button @dblclick="changeName">{{name}}</button>
      <br />
      <img src="./assets/vue.svg" alt="" :class="show" />
      <button @click="changeShow">Ocultar</button>
    </div>
    <Footer />
  </div>
</template>

<style scoped>
.show{
  display: block;
}
.hidden{
  display: none;
}
</style>
