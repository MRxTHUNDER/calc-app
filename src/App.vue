<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <h2> Welcome to MY CALC app</h2>
    <CalApp
      @button-clicked="handleButtonClick"
      @operator-selected="handleOperatorSelected"
      @calculation-completed="handleCalculationCompleted"
    />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import CalApp from './components/CalApp.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    CalApp,
  },
  methods: {
    handleButtonClick(value) {
      console.log('Button clicked:', value);
    },
    handleOperatorSelected(operator) {
      console.log('Operator selected:', operator);
    },
    handleCalculationCompleted(result) {
      console.log('Calculation completed:', result);
    }
  }
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
</style>
