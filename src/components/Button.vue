<template>
  <button class="button" v-on="$listeners">
    <slot />
  </button>
</template>

<style lang="scss" scoped>
.button {
  width: 100%;
  display: block;
  border: 0;
  box-shadow: none;
  min-height: rem(65px);
  color: $color_primary;
  background: white;
  transition: opacity 200ms ease-in, transform 100ms ease-in;
  cursor: pointer;

  & + & {
    margin-top: rem(25px);
  }

  &:focus,
  &:focus-within {
    outline: 2px solid white;
    outline-offset: 3px;
  }

  &:active {
    transform: scale(0.98);
  }

  &:disabled {
    opacity: 0.45;
    cursor: not-allowed;
  }
}
</style>
