<template>
  <div class="hello" @keyup.enter="enterKeyHit">
    <label for="username">Username: </label>
    <input type="text" id="username" v-model="username" />
    <label for="password">Password</label>
    <input type="password" id="password" v-model="password" />
    <button>Login</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      username: null,
      password: null
    }
  },
  methods: {
    enterKeyHit () {
      console.log('enter key hit')
      if (this.username === 'admin' && this.password === 'admin') {
        this.$router.push({ name: 'Dashboard' })
      // eslint-disable-next-line brace-style
      }
      else {
        alert('Wrong username or password')
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
