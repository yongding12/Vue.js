//过滤器应用:将第一个小写字母过滤后成大写字母
<template>
  <div id="demo6">
    {{ message | capitalize }}<br/>
    <input v-model="message">
  </div>
</template>

<script>
  export default{
    name: 'demo6',
    data () {
      return {
        message: 'hello'
      }
    },
    filters: {
      capitalize: function (value) {
        if (!value) return ''
        value = value.toString()
        return value.charAt(0).toUpperCase() + value.slice(1)
      }
    }
  }
</script>
