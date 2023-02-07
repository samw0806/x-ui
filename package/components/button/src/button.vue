<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <button
      class="x-button"
      :class="[
        `x-button-${type}`,
        {
          disabled: disabled,
          plain: plain,
          round: round,
          mimicry: mimicry,
          circle: circle,
        },
      ]"
      :disabled="disabled"
    >
      <slot></slot>
    </button>
  </div>
</template>

<script lang="ts" setup name="xButton">
defineProps({
  type: {
    type: String,
    default: "default",
  },
  plain: {
    type: Boolean,
    default: false,
  },
  circle: {
    type: Boolean,
    default: false,
  },
  round: {
    type: Boolean,
    default: false,
  },
  icon: {
    type: String,
    default: "",
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  mimicry: {
    type: Boolean,
    default: false,
  },
});
</script>
<style scoped lang="scss">
@import "./button.scss";
</style>
