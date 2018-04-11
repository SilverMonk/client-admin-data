<template>
  <div class="page-container">
    <el-form :model="projectInfo" :rules="rules" ref="projectInfo" label-width="100px" class="project_info">
      <el-form-item label="活动名称" prop="name">
        <el-input v-model="projectInfo.name"></el-input>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'project',
  data() {
    return {
      projectInfo: {
        name: ''
      },
      rules: {
        name: [
          { required: true, message: '请输入活动名称', trigger: 'blur' },
          { min: 3, max: 5, message: '长度在 3 到 5 个字符', trigger: 'blur' }
        ]
      }
    };
  },
  methods: {}
};
</script>

<style rel="stylesheet/scss" lang="scss">

</style>
