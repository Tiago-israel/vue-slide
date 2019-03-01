<template>
  <b-col sm md="4" offset-md="4">
    <carousel :paginationEnabled="false" :perPage="1.2">
      <slide v-for="(item, index) in list" :key="index">
        <b-col cols="12">
          <b-card
            title="Card Title"
            :img-src="'https://randomuser.me/api/portraits/men/'+index+'.jpg'"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</b-card-text>
            <b-button href="#" variant="primary">Go somewhere</b-button>
          </b-card>
        </b-col>
      </slide>
    </carousel>
  </b-col>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: () => ({
    list: [1, 2, 3, 4, 5, 6, 7]
  }),
  components: {
    Carousel,
    Slide
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
