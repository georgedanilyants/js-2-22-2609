<template>
    <div class="catalog__item">
        <button 
            class="catalog__bucket" 
            name="add"
            @click="addItem(item)">
            <img class="catalog__hidden_img" 
            src="https://raw.githubusercontent.com/Eliseev88/geekbrains/3fdc76c4d5e84b1398b168e6239b8651dce01f6f/products/Forma_1_copy.svg" alt="#">
            <span class="catalog__hidden_text">Add to Cart</span>
        </button>
        <div class="catalog__photo">
            <img class="catalog__img" :src="item.productImg" alt="#">
        </div>
        <div class="catalog__content">
            <a class="catalog__name" href="#">{{item.productName}}</a>
            <div class="catalog__price">${{item.productPrice}}.00</div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['item'],
      methods: {
        addItem(product) {
                this.$store.commit("addItem", product);
        },
      }
}
</script>

<style>

</style>

