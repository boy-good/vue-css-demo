<template>
  <div>
    <div class="box">{{ $t("name") }}</div>
    <div class="box">mm</div>
    <div class="box" @click="check('zh')">中文</div>
    <div class="box" @click="check('en')">英文</div>
  </div>
</template>
<script>
export default {
  name: "About",
  components: {},
  mounted() {},
  data() {
    return {};
  },
  methods: {
    check(type) {
      window.localStorage.setItem("locale", type);
      this.$i18n.locale = type;
    },
  },
  filters: {},
};
</script>
<style lang="less">
.box {
  width: 100px;
  height: 100px;
  background-color: aqua;
}
</style>
