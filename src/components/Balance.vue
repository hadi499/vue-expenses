<script setup>
import { defineProps } from 'vue';
const props = defineProps({
  total: {
    type: Number,
    required: true
  }
})

</script>

<template>
  <h4>Your Balance</h4>

  <h1 v-if="total < 0" id="balance">- ${{ Math.abs(total) }}</h1>

  <h1 v-else id="balance">+ ${{ total }}</h1>
</template>
