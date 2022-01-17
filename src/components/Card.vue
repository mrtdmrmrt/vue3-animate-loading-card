<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="cards">
    <div class="card">
      <div class="image">
        <img src="https://via.placeholder.com/300x250" alt="" />
      </div>
      <div class="content">
        <h2>Title</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Beatae
          voluptatibus odit dicta ratione saepe aperiam qui!
        </p>
      </div>
    </div>

    <div class="card is-loading">
      <div class="image">
        <img src="" alt="" />
      </div>
      <div class="content">
        <h2></h2>
        <p></p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.cards {
  display: flex;
}
.card {
  margin: 10px;
  width: 300px;
  background: #fff;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
  .image img {
    max-width: 100%;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
  }
  .content {
    padding: 20px 30px;
  }
}
.card.is-loading {
  .image,
  h2,
  p {
    background: #eee;
    background: linear-gradient(110deg, #ececec 8%, #f6f6f6 18%, #ececec 33%);
    border-radius: 5px;
    background-size: 200% 100%;
    animation: 1.5s shine linear infinite;
  }
  .image {
    height: 250px;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
  }
  h2 {
    height: 50px;
  }
  p {
    height: 70px;
  }
}
@keyframes shine{
    to{
        background-position-x: -200%;
    }
}
</style>
