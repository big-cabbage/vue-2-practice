<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <br>
    <br>
    <img :src="url">
    <button v-on:click="run1()">first method</button>
    <button @click="run2()">second method</button>
    <br>
    <br>
    <button @click="getMsg()">get Msg method</button>
    <br>
    <button @click="setMsg()">set Msg method</button>
    <br>
    <button @click="requestData()">get data method</button>
    <ul>
      <li v-for="item in list">
        {{item}}
      </li>
    </ul>
    <br>
    <button @click="requestData()">get data method</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
        url: '123',
        list: [],
    }
  },
  methods: {
      run1 () {
          alert('this is a method');
      },
      run2 () {
          alert('this is another function');
      },
      getMsg() {
          alert(this.msg)
      },
      setMsg () {
          this.msg = '12123'
      },
      requestData () {
          for (let i=0; i<10; i++){
              this.list.push('i am ' + i + ' item!');
          }
      }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
