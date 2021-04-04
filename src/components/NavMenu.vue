<template>
  <div id="NavMenu">
    <el-row :gutter="20">
      <el-col :span="4" style="background: #e4e7ed"
        ><a href="/" style="text-decoration: none; font-size: 40px">
          <img src="pic/logo.png" style="height: 50px" />上线管理平台</a
        ></el-col
      >

      <el-col :span="7">
        <el-menu
          :default-active="activeIndex"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          routerpx
        >
          <el-menu-item index="1" style="font-size: 1.2em"
            ><i class="el-icon-s-home"></i>处理中心</el-menu-item
          >
          <el-menu-item index="2" style="font-size: 1.2em"
            ><i class="el-icon-warning-outline"></i>我的任务</el-menu-item
          >
          <el-menu-item index="3" style="font-size: 1.2em"
            ><i class="el-icon-user"></i>项目成员</el-menu-item
          >
          <el-menu-item index="4" style="font-size: 1.2em"
            ><i class="el-icon-setting"></i>系统设置</el-menu-item
          >
        </el-menu>
      </el-col>

      <el-col :span="1" :offset="8">
          <el-badge :value="12" class="item" style="margin-top:1.2em" >
          <el-button size="medium">消息</el-button>
          </el-badge>
      </el-col>

      <el-col :span="4"  > 
          <el-button type="primary" style="width:40%;margin-top:1em">登陆</el-button>
          <el-button type="primary" style="width:40%;">退出</el-button>
      </el-col>
    </el-row>
  </div>
</template>


<script>
export default {
  data() {
    return {
      activeIndex: "1",
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style>
#NavMenu {
  margin-top: 0;
}
.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }

}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
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