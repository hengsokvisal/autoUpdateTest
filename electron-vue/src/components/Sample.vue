<template>
  <div>
  <h1>Hello This is Visal</h1>
   Version: <span id="version">v0.1.9</span>
    <!-- the button onClick sends a quitAndInstall message to the electron main process -->
    <button ref="btn" @click="click" id="ready">{{ hello }}</button>
  </div>
</template>

<script>
const ipcRenderer = require('electron').ipcRenderer

export default {
  name: 'Sample',
  data: function () {
    return {
      test: '99',
      hello: "ok"
      
    }
  },
  methods: {
    click () {
      var btn = this.$refs.btn
      console.log(btn)
      this.hello = 'ko'
    }
  }
}
</script>

<style scoped>
</style>
