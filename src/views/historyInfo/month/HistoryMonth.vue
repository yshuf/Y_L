<template>
  <el-container>
    <el-header style="text-align: right; font-size: 16px;">
      <el-menu
        :default-active="activeIndex"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        router
      >
       <el-menu-item><el-page-header @back="goBack" style="margin-top: 18px;"></el-page-header></el-menu-item>
        <el-menu-item index="/index/historyMonth/yulinMonth">渔林</el-menu-item>
      </el-menu>
    </el-header>

    <el-main>
      <router-view></router-view>
    </el-main>
  </el-container>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: "1"
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    goBack(){
      this.$router.go(-1);
    }
  }
};
</script>

<style scoped>
.el-header {
 background-color: #f6fcd7;
  /* color: #333; */
  line-height: 60px;
  border-radius: 100px;
  font-weight: 700;
  font-size: 30px;
}

.el-menu {
  background-color: #f7fdd5;
}

.el-main::-webkit-scrollbar {
  display: none;
}
</style>

