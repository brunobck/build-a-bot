<template>
  <div>
    <div class="header">
      <span v-if="open" @click="open = !open">&#x25B2; Collpse</span>
      <span v-if="!open" @click="open = !open">&#x25BC; Expand</span>
    </div>
    <slot v-if="open">Default content</slot>
  </div>
</template>

<script>
export default {
  name: 'CollapsibleSection',
  data() {
    return {
      open: true,
    };
  },
};
</script>

<style scroped>
.header {
  background-color: #bbb;
  padding: 3%;
  cursor: pointer;
}
</style>
