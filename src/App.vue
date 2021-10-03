<template>
<p class="text" >{{ title }}</p>
<input type="text" ref="testref">
<button v-on:click="handleClick">Go find it !</button>
<Modal />
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
</template>

<script>
import Modal from './components/Modal.vue'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  components: { Modal },
  name: 'App',
  data () {
    return {title: 'Seaaarch'}
  },
  methods: {
    handleClick(){
      this.$refs.testref.classList.add('active')
      this.$refs.testref.focus()
    }
  }
  // components: {
  //   HelloWorld
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.text{
  background-color: burlywood;
  font-size: 30pt;
}
</style>
