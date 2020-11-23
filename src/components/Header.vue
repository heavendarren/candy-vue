<template>
  <div id="head">

    <el-container>
      <el-header>
        <div class="logo">
          <img src="./assets/img/toplogo.png" alt="">
        </div>
        <el-menu :default-active="defaltActive"
                 class="el-menu-demo"
                 mode="horizontal"
                 @select="handleSelect"
                 :router="router"
        >
          <el-menu-item index="/">首页</el-menu-item>
          <el-menu-item index="/">新闻咨询</el-menu-item>
          <el-menu-item index="/">产品中心</el-menu-item>
          <el-menu-item index="/">走进我们</el-menu-item>
          <el-menu-item index="/">我的</el-menu-item>

        </el-menu>
      </el-header>
    </el-container>
  </div>
</template>
<script>
export default {
  data () {
    return {
      router: true,
      defaultActive: '/',
      isShow: false
    }
  },
  methods: {
    handleSelect (key) {
      // eslint-disable-next-line eqeqeq
      this.isShow = this.defaultActive != key
      console.log(this.isShow)
    }
  }
}

</script>
