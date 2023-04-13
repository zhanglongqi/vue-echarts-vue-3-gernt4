<script setup lang="ts">
import { ref, onMounted } from 'vue';
import power from './components/power.vue';

const power_value = ref(100.45);

onMounted(() => {
  setInterval(() => {
    power_value.value = Math.round(Math.random() * 100);
  }, 2000);
});
</script>
<template>
  <power :value="Math.round(power_value)" />
</template>
