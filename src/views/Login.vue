<template>
  <div class="login-box">
    <h2>Vue3 Element-Plus Admin</h2>
    <el-form class="login-form" :model="loginForm">
      <el-form-item label="账号">
        <el-input v-model="loginForm.username" />
      </el-form-item>
      <el-form-item label="密码">
        <el-input type="password" v-model="loginForm.password" />
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">登录</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const loginForm = reactive({
  username: '',
  password: ''
})

</script>

<style lang="less" scoped>
.login-box {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .login-form {
    width: 520px;

    .el-form-item {
      width: 100%;
    }
  }
}
</style>
