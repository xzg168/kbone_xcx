<template>
  <div class="footer">
    <mt-tabbar v-model="selected">
      <mt-tab-item id="register">
        <img slot="icon" src="../assets/reg.png">
        登记
      </mt-tab-item>
      <mt-tab-item id="orders">
        <img slot="icon" src="../assets/order.png">
        订单
      </mt-tab-item>
      <mt-tab-item id="person">
        <img slot="icon" src="../assets/person.png">
        我的
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      selected: 'register'
    }
  },
  watch: {
    selected(val) {
      console.log(val)
      if (val === 'register') {
        // window.location.href = '/register'
        window.open('/register')
        // this.$router.push({
        //   name: 'Register'
        // })
      }
    }
  }
}
</script>

<style lang="less">
.footer {
  width: 100%;
  text-align: center;
  img{
    height: 24px;
  }
  .mint-tab-item{
    height: 35px;
  }
}
</style>
