<template>
  <div class="loginBox">
    <el-form ref="loginRef" :model="loginForm">
      <el-form-item>
        <el-input
            v-model="loginForm.username"
            type="text"
            placeholder="账号">
          <template #prefix><span class="inputLabel">账号</span></template>
        </el-input>
      </el-form-item>
      <el-form-item>
        <el-input
            v-model="loginForm.password"
            type="password"
            placeholder="请输入密码">
          <template #prefix><span class="inputLabel">密码</span></template>
        </el-input>
      </el-form-item>
      <el-form-item>
        <el-button
            :loading="loading"
            size="large"
            type="primary"
            style="width:100%;"
        >
          <span v-if="!loading">登 录</span>
          <span v-else>登 录 中...</span>
        </el-button>

      </el-form-item>
    </el-form>
  </div>
</template>

<script setup>
import {ref} from 'vue';

const loginForm = ref({
  username: '',
  password: ''
});
// 加载
const loading = ref(false);

</script>

<style lang='scss' scoped>
.loginBox {
  width: 100%;
  height: 400px;
  background-color: cadetblue;
  position: relative;
  left: 50%;
  top: 50%;
  transform: translate(-50%,-50%);
}

.inputLabel {
  margin: 0px 10px 30px auto;
  text-align: center;
  color: #313131;
}

.el-form {

  .el-input{
    input {

    }
  }
}

//.title {
//  margin: 0px auto 30px auto;
//  text-align: center;
//  color: #707070;
//}
//


//  .input-icon {
//    height: 39px;
//    width: 14px;
//    margin-left: 0px;
//  }
//}
//.login-tip {
//  font-size: 13px;
//  text-align: center;
//  color: #bfbfbf;
//}
//.login-code {
//  width: 33%;
//  height: 40px;
//  float: right;
//  img {
//    cursor: pointer;
//    vertical-align: middle;
//  }
//}
//.el-login-footer {
//  height: 40px;
//  line-height: 40px;
//  position: fixed;
//  bottom: 0;
//  width: 100%;
//  text-align: center;
//  color: #fff;
//  font-family: Arial;
//  font-size: 12px;
//  letter-spacing: 1px;
//}
//.login-code-img {
//  height: 40px;
//  padding-left: 12px;
//}
</style>
