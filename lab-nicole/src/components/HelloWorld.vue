<template>
  <div class="hello">
    {{ msg }}
    {{ question }}
    <p>Who am I speaking with?:</p>
    <p> {{ name }}</p>
    <input v-model="name" placeholder="name">
    <p>How many pets would you like to own?</p>
    {{ pets }} <button v-on:click="pets -=1">-</button> <button v-on:click="pets += 1">+</button>
    <br><br>
    <button v-on:click="peace">I'm done with you!</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Hello World!',
      name: '',
      pets: 0
    }
  },
  methods: {
    peace: function () {
      alert('Sad to see you go!')
    }
  }
}
</script>
