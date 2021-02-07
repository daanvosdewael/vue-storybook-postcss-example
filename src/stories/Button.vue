<template>
  <button type="button" @click="onClick">{{ label }}</button>
</template>

<script>
export default {
  name: 'my-button',

  props: {
    label: {
      type: String,
      required: true,
    },
  },

  methods: {
    onClick() {
      this.$emit('onClick');
    },
  },
};
</script>

<style lang="postcss" scoped>
button {
  appearance: none;
  border: 0;
  font-size: 18px;

  &::before {
    content: '> ';
  }

  &::after {
    content: ' <';
  }
}
</style>