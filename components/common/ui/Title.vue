<template>
  <h2 v-if="title" class="c-title__title text-5xl text-black font-normal">
    <span class="text-primary text-7xl">{{ firstLetter }}</span>
    {{ restLetter }}
  </h2>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
  computed: {
    firstLetter() {
      return this.title.charAt(0)
    },
    restLetter() {
      return this.title.slice(1)
    },
  },
}
</script>

<style lang="scss" scoped>
.c-title {
  font-family: Yu Mincho Medium, YuMincho, serif;
  line-height: 110px;
}
</style>
