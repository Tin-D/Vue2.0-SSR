<!-- home.vue -->
<template>
  <div>
    home2
    <div class="home">{{ homeInfo }}</div>
    <img src="https://upload.jianshu.io/users/upload_avatars/8958489/68d15acc-f8a4-4661-830e-8374af2953d9.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/80/h/80/format/webp"/>
  </div>
</template>


<script>
export default {
  serverRequest(store) {
    return store.dispatch("getHomeInfo");
  },
  mounted() {},
  computed: {
    homeInfo() {
      return this.$store.state.homeInfo;
    },
  },
};
</script>

<style scoped>
.home{
    font-size: 50px;
    color: red;
}
</style>