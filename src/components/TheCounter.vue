<script setup lang="ts">
import { useCounterStore } from '~/stores/counter'

const counter = useCounterStore()

const { count } = storeToRefs(counter)
</script>

<template>
  <div flex items-center justify-center gap-8>
    <div class="count-btn" @click="counter.dec()">
      -
    </div>
    <span font-mono>{{ count }}</span>
    <div class="count-btn" @click="counter.inc()">
      +
    </div>
  </div>
</template>

<style lang="scss" scoped>
.count-btn {
  @apply: h-8 w-8 center rd-full p-0 btn;
}
</style>
