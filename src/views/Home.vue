<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>Hello!</h1>
    <p>{{ num }}</p>
    <button v-on:click="randomAdd(num)">Random Add</button>
    <p class="warning" v-if="num % 3 === 0">Multiple of 3</p>
  </div>
</template>

<style>
.warning {
  color: red;
}
</style>

<script>
export default {
  data: function() {
    return {
      message: "Hello!",
      num: 0
    };
  },
  methods: {
    randomAdd: function(num) {
      var min = 1;
      var max = 4;
      var rando = Math.random() * (+max - +min) + +min;
      var rindo = Math.floor(rando);
      this.num += rindo;
      console.log(this.num);
    }
  }
};
</script>
