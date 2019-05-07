<template>
  <section class="container">
    <el-card style="flex:1">
      <div slot="header" class="clearfix">
        <span>Login</span>
      </div>
      <form>
        <div class="form-content">
          <span>User ID</span>
          <el-input placeholder="" v-model="formData.id"></el-input>
        </div>
        <div class="form-content">
          <el-checkbox v-model="isCreateMode">アカウント作成</el-checkbox>
        </div>
        <div class="text-right">
          <el-button type="primary">{{buttonText}}</el-button>
        </div>
      </form>
    </el-card>
  </section>
</template>

<script>
export default {
  asyncData() {
    return{
      isCreateMode: false,
      formData: {
        id: ''
      }
    }
  },
  computed: {
    buttonText(){
      return this.isCreateMode ? '新規作成' : 'ログイン'
    }
  }
}
</script>

<style scoped>
.form-content {
  margin: 16px 0;
}
</style>
