<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <h3>welcome to i tunes</h3>
    <p>{{count}}</p>

    <button @click="increaseCounter">Increase Count</button>
    <button @click="decreaseCounter">decrease Count</button>
    <p v-for="name in names" :key='name'>{{name}}</p>
    <p v-if='awesome'>this statement is true</p>
    <p v-else> this statement is false</p>
  </div>
</template>

<script>
// const axios = require('axios');
// const API ="https://itunes.apple.com/search?term=radiohead"

export default {
  name: 'Home',
  data(){
    return{
      api_url: "https://itunes.apple.com/search?term=radiohead",
      count: 0,
      names:['collins', 'yego', 'kipkemoi'],
      awesome: true
    }
  },
  methods: {
   
      increaseCounter(){
        this.count +=1

      },
      decreaseCounter(){
        this.count *=2
      },
    }
  }
  


</script>
