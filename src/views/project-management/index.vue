<template>
  <div class="dashboard-editor-container">
        <el-row style="padding:16px 16px 0;margin-bottom:30px;">
            <template>
            <router-link :to="'/dashboard'">
                <el-button type="primary" size="large" icon="el-icon-edit">
                新建一个项目
                </el-button>
            </router-link>
            </template>
        </el-row>

        <el-row :gutter="30">
            <el-col :xs="{span: 24}" :sm="{span: 12}" :md="{span: 12}" :lg="{span: 6}" :xl="{span: 6}" style="margin-bottom:30px;">
                <ProjectBox />
            </el-col>
            <el-col :xs="{span: 24}" :sm="{span: 12}" :md="{span: 12}" :lg="{span: 6}" :xl="{span: 6}" style="margin-bottom:30px;">
                <ProjectBox />
            </el-col>
        </el-row>
  </div>
</template>

<script>
import ProjectBox from './components/ProjectBox'

export default {
  name: 'ProjectList',
  components: {
    ProjectBox
  }
}
</script>

<style lang="scss" scoped>
.dashboard-editor-container {
  padding: 32px;
  background-color: rgb(240, 242, 245);
  position: relative;

  .github-corner {
    position: absolute;
    top: 0px;
    border: 0;
    right: 0;
  }

  .chart-wrapper {
    background: #fff;
    padding: 16px 16px 0;
    margin-bottom: 32px;
  }
}

@media (max-width:1024px) {
  .chart-wrapper {
    padding: 8px;
  }
}
</style>
