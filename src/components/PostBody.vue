<template>
  <div class="wrap">
    <div class="comment-count">
      {{ commentCount }} 评论
    </div>
  </div>
</template>

<script>
export default {
  name: 'PostBody',
  props: ['title'],
  computed: {
    commentCount() {
      return this.$store.state.comment.all.length
    }
  }
}
</script>

<style scoped>
.wrap {
  height: 200px;
  margin: 20px auto;
  width: 400px;
  position: relative;
  background-color: #fff;
}

.comment-count {
  position: absolute;
  bottom: 10px;
  right: 10px;
  border-bottom: 1px solid gray;
}
</style>
