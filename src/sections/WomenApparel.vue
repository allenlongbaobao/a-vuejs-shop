<template>
  <transition name="fade" tag="div">
  <div class="product-page">
    <div class="sidebar-wrap">
      <Sidebar category="womenApparel"/>
    </div>
    <div class="product-list-wrap">
      <h1>Women Apparel</h1>
      <ProductList category="womenApparel"/>
    </div>
  </div>
</transition>
</template>

<script>
import ProductList from '@/components/ProductList'
import Sidebar from '@/components/Sidebar'

export default {
  name: 'index',
  bannerLink: '../static/images/menApparelBanner.jpg',
  components: {
    ProductList,
    Sidebar
  },
  created () {
    this.$store.commit('setBannerLink', this.$options.bannerLink)
  }
}
</script>

<style lang="css">
 h1 {
  text-align: left;
  margin-bottom: 40px;
  font-size: 20px;
 }
</style>
