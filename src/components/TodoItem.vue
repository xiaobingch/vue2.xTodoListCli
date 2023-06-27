<template>
  <li class="item" @click="handleDelete">{{ content }}</li>
</template>

<script>
export default{
  props: ['content', 'index'],
  methods: {
    handleDelete() {
      this.$emit('delete', this.index)
    }
  }
}
</script>
<!-- 局部样式 scoped -->
<style scoped>
  .item{
    color: green;
  }
</style>
