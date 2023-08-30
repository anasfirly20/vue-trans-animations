<template>
  <button type="button" @click="toggle">Toggle</button>
  <transition name="fade">
    <h2 v-if="flag">Hello world!</h2>
  </transition>
</template>

<script>
export default {
  name: "App",
  data(){
    return {
      flag: false
    }
  },
  methods: {
    toggle(){
      this.flag = !this.flag
    }
  }
}
</script>

<style>
.fade-enter-from{
  opacity: 0;
}

.fade-enter-active {
  transition: all 0.25s linear;
}

.fade-leave-to{
  transition: all 0.25s linear;
  opacity: 0;
}

</style>