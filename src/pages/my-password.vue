<template>
  <div>
    <d-header>密码管理</d-header>
    <group :gutter="0">
      <cell title="登录密码"
        :value="dataInfo.IsLoginPassword ? '' : '暂无密码'"
        :link="{
          name: 'CheckPhone',
          params: {
            smsType: 5,
            nextPath: 'set-password'
          }
        }"></cell>
      <cell title="交易密码"
        :value="dataInfo.IsSellPassword ? '' : '暂无密码'"
        :link="{
          name: 'CheckPhone',
          params: {
            smsType: 5,
            nextPath: 'set-tran-pwd'
          }
        }"></cell>
    </group>
  </div>
</template>
<script>
export default {
  computed: {
    dataInfo() {
      return this.$store.state.UserInfo
    }
  }
}
</script>
