<script setup>
let show = $ref(true)
</script>

<template>
  <div class="demo">
    <button @click="show = !show">切换</button>
    <Transition name="fade">
      <p style="margin-top: 20px" v-if="show">你好</p>
    </Transition>
  </div>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
