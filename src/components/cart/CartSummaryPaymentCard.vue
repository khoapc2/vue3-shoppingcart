<template>
  <div class="cart-item-card">
    <h3>
      Cart Total:
      {{
        cart_total.toLocaleString("it-IT", {
          style: "currency",
          currency: "VND",
        })
      }}
    </h3>
    <button class="view-product-button">Pay by Credit Cardd</button>
  </div>
</template>

<script>
export default {
  computed: {
    cart_total() {
      return this.$store.getters.cartTotal;
    },
  },
};
</script>
