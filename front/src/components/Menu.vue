
<template>
  <el-menu
    :default-active="activeIndex"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
  >
    <el-menu-item index="1">处理中心</el-menu-item>
    <el-submenu index="2">
      <template #title>我的工作台</template>
      <el-menu-item index="2-1">选项1</el-menu-item>
      <el-menu-item index="2-2">选项2</el-menu-item>
      <el-menu-item index="2-3">选项3</el-menu-item>
      <!-- <el-submenu index="2-4">
        <template #title>选项4</template>
        <el-menu-item index="2-4-1">选项1</el-menu-item>
        <el-menu-item index="2-4-2">选项2</el-menu-item>
        <el-menu-item index="2-4-3">选项3</el-menu-item>
      </el-submenu> -->
    </el-submenu>
    <!-- <el-menu-item index="3" disabled>消息中心</el-menu-item> -->
    <!-- <el-menu-item index="4"
      ><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item
    > -->
    <el-submenu index="5" class="fr">
      <template #title>
        <i class="el-icon-user-solid"></i>
        登录
      </template>
      <el-menu-item index="5-1">修改密码</el-menu-item>
      <el-menu-item index="5-2">退出登录</el-menu-item>
    </el-submenu>
  </el-menu>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1',
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style  scoped>
.fr {
  float: right !important;
}
/* .el-menu-item, .el-submenu{
  text-align: left;
} */
</style>