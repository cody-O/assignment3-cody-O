<template>
  <div class="syrup"
  :style="{
      backgroundColor: props.syrup.color,
      opacity: props.syrup.name === 'No Syrup' ? 0 : 0.25
    }"></div>
</template>

<script setup lang="ts">
import type { SyrupType } from "../stores/beverage";

const props = defineProps<{
  syrup: SyrupType;
}>();
</script>

<style lang="scss" scoped>
.syrup {
  transform: translateY(400%);
  background-color: #c6c6c6;
  position: relative;
  width: 100%;
  height: 20%;
  animation: pour-tea 2s 1s forwards;
  z-index: 2;
}
</style>
