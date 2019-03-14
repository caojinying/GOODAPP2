<template>
<div>
<x-header :right-options="{showMore: false}" :left-options="{showBack: false}">登陆</x-header>
<x-input title="手机号码格式化" mask="999 9999 9999" v-model="phone" :max="13" is-type="china-mobile"></x-input>
<x-input title="密码" :max="13"></x-input>
<x-button @click.native="login">登陆</x-button>
</div>
</template>

<script>
import { XInput, XButton, XHeader } from 'vux'

export default {
  components: {
    XInput,
    XButton,
    XHeader
  },
  name: 'HelloWorld',
  methods: {
    login () {
      this.$router.push('/Login')
    }
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.comtainer{
padding: 15px;
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