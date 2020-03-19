<template>
  <div>
    <h1>{{ message | fallback | uppercase }}</h1>
    <a @click="handleClick">Click me!</a>
  </div>
</template>

<script>
export default {
  filters: {
    fallback(message) {
      return message || 'Hola Mundo'
    },
    uppercase(message) {
      return message.toUpperCase()
    }
  },
  data() {
    return {
      message: 'Hello World!'
    }
  },
  methods: {
    handleClick(event) {
      this.message = 'Curious little monkey!'
    }
  }
}
</script>
