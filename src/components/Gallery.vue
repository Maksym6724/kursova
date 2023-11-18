<template>
  <h1 class="">Gallery</h1>
  <div class="gallery">
    <img src="https://picsum.photos/id/1028/300/300" alt="a forest after an apocalypse">
    <img src="https://picsum.photos/id/15/300/300" alt="a waterfall and many rocks">
    <img src="https://picsum.photos/id/1040/300/300" alt="a house on a mountain">
    <img src="https://picsum.photos/id/106/300/300" alt="sime pink flowers">
    <img src="https://picsum.photos/id/136/300/300" alt="big rocks with some trees">
    <img src="https://picsum.photos/id/1039/300/300" alt="a waterfall, a lot of tree and a great view from the sky">
    <img src="https://picsum.photos/id/110/300/300" alt="a cool landscape">
    <img src="https://picsum.photos/id/1047/300/300" alt="inside a town between two big buildings">
    <img src="https://picsum.photos/id/1057/300/300" alt="a great view of the sea above the mountain">
  </div>
</template>

<script>
export default {
name: "Gallery"
}
</script>

<style scoped>
.gallery {
  --s: 150px; /* control the size */
  --g: 10px;  /* control the gap */
  --f: 1.5;   /* control the scale factor */

  display: grid;
  gap: var(--g);
  width: 1024px;
  aspect-ratio: 1;
  grid-template-columns: repeat(3,auto);
}

.gallery > img {
  width: 0;
  height: 0;
  min-height: 100%;
  min-width: 100%;
  object-fit: cover;
  cursor: pointer;
  filter: grayscale(80%);
  transition: .35s linear;
}

.gallery img:hover{
  filter: grayscale(0);
  width:  calc(var(--s)*var(--f));
  height: calc(var(--s)*var(--f));
}


body {
  margin: 0;
  min-height: 100vh;
  display: grid;
  place-content: center;
  background: #60c4ff;
}
</style>