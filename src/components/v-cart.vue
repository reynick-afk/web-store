<!-- Vue Cart -->
<template>
  <div class="v-cart">
    <h1>Cart</h1>
    <v-cart-item
    v-for="item in cart_data"
    :key="item.article"
    :cart_item_data="item"
    />
  </div>
</template>

<script>
import vCartItem from './v-cart-item.vue'

export default {
  name: "v-cart",
  props: {
    
    cart_data:{
      type: Array,
        default() {
          return []
    }
  }
},
  components: {
    vCartItem
  },
  data () {
    return {
    }
  }
}
</script>

<style lang='scss'>

</style>
