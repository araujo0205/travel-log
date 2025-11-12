<script lang="ts" setup>
const colorMode = useColorMode();

const isDark = computed({
  get: () => colorMode.value === "dark",
  set: (value: boolean) => {
    colorMode.preference = value ? "dark" : "light";
  },
});
</script>

<template>
  <label class="swap swap-rotate mx-4">
    <input v-model="isDark" type="checkbox">
    <icon class="swap-on" name="tabler:sun" size="24" />
    <icon class="swap-off" name="tabler:moon-filled" size="24" />

  </label>
</template>
