<template>
  <div class="home">
    <el-container>
      <el-header>
        <el-row :gutter="20">
          <el-col :span="4">
            <div class="grid-content bg-purple"></div>
          </el-col>
          <el-col :span="16">
            <div class="grid-content bg-purple">
              <el-menu
                :default-active="activeIndex"
                class="el-menu-demo"
                mode="horizontal"
                @select="handleSelect"
              >
                <el-menu-item index="1"><router-link to="/index">处理中心</router-link></el-menu-item>
                <el-submenu index="2">
                  <template slot="title">我的工作台</template>
                </el-submenu>
                <el-menu-item index="3"><router-link to="/index">消息中心</router-link></el-menu-item>
                <el-menu-item index="4">
                  <a href="" target="_blank">订单管理</a>
                </el-menu-item>
              </el-menu>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple"></div>
          </el-col>
        </el-row>
      </el-header>
      <el-main style="margin-top: 20px">
        <el-row :gutter="20">
          <el-col :span="4">
            <div class="grid-content bg-purple"></div>
          </el-col>
          <el-col :span="16">
            <div class="grid-content bg-purple">
              <router-view></router-view>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple"></div>
          </el-col>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "home",
  components: {},
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
<style>
.el-row {
  margin-bottom: 20px;
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}

.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
