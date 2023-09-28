<script setup lang="ts">
import { computed, ref, shallowReactive } from "vue";

const number = ref(80)
const showOrNot = computed(
  (): boolean => {
    let showOrNot = false
    const rand = Math.round(Math.random() * 100)
    if(rand >= 50) {
      showOrNot = true
    }
    return showOrNot
  }
)
</script>

<template>
  <p v-if="number >= 50">あ</p>
  <p v-if="Math.round(Math.random() * 100) >= 50">い</p>
  <p v-if="showOrNot">う</p>
</template>
