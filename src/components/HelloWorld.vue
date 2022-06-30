<template>
  <v-container class="main-image-container">
    <v-row class="main-image-container">
      <carousel-3d :inverse-scaling="900" :space="800" :autoplay="true" :autoplay-timeout="5000" :width="900" :height="500">
        <slide
          v-for="(item, i) in randomPics"
          :key="i"
          :src="item.src"
          :index="i"
        >
        <v-img 
        class="main-image-container"
            :src="item.src"></v-img>
        </slide>
      </carousel-3d>
    </v-row>
  </v-container>
</template>

<script>
import { Carousel3d, Slide } from "vue-carousel-3d";

export default {
  name: "HelloWorld",
  components: {
    Carousel3d,
    Slide,
  },

  data: () => ({
    items: [
      {
        src: "https://prismacake.s3.amazonaws.com/.1pastelBoda.jpg",
      },
      {
        src: "https://prismacake.s3.amazonaws.com/.1pastelBoda.jpg",
      },
      {
        src: "https://prismacake.s3.amazonaws.com/.1pastelBoda.jpg",
      },
      {
        src: "https://prismacake.s3.amazonaws.com/.1pastelBoda.jpg",
      },
    ],
    randomPics: [
      {
        src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
      },
      {
        src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
      },
      {
        src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
      },
      {
        src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
      },
      {
        src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
      },
    ],
  }),
};
</script>
<style>

.main-image-container{
  height: 100%;
}

</style>
