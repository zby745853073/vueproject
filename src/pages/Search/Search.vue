<template>
  <section class="search">
    <HeaderTop title='搜索'>
      <template v-slot:search>
        <router-link class='header_search' to='/msite'>
          <i class='iconfont icon-fanhui'></i>
        </router-link>
      </template>
    </HeaderTop>
    <form class="search_form" action="#">
      <input type="search" name="search" placeholder="请输入商家或美食名称" class="search_input" />
      <input type="submit" name="submit" class="search_submit" />
    </form>
  </section>
</template>

<script>
import HeaderTop from "../../components/HeaderTop/HeaderTop.vue";
export default {
  components: {
    HeaderTop
  }
};
</script>

<style  scoped lang='scss'>
@import "../../common/styles/mixins.scss";
.search_form {
  *zoom: 1;
  margin-top: 45px;
  background-color: #fff;
  padding: 12px 8px;
  @include clearFix();
  input.search_input {
    float: left;
    width: 79%;
    border: 4px solid #f2f2f2;
    font-size: 14px;
    color: #333;
    background-color: #f2f2f2;
  }
  input.search_submit {
    float: right;
    width: 18%;
    border: 4px solid #02a774;
    font-size: 16px;
    color: #fff;
    background-color: #02a774;
  }
}
</style>