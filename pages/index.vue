<template>
    <div class="container">
        <h1> {{name }} Page </h1>
        <div class="container">
            <nuxt-link to="/about">About Page</nuxt-link>
        </div>
    </div>
</template>

<script>
export default {
  asyncData() {
    return new Promise((resolve) =>{
      setTimeout(() => {
        resolve({ name : 'About'})
      }, 1000);
    })
  },
}
</script>


<style scoped>
.container {
  font-size: 20px;
  text-align: center;
  padding-top: 100px;
}
</style>