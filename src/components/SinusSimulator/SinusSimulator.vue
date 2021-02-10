<template>
  <v-container fluid id="3DPrinting" class="blue--text grey lighten-2">
    <h1 align="center">3D - Printing</h1>
    <v-container  class="pa-5">
      <vueper-slides fade progress autoplay fixed-height="500px">
        <vueper-slide
            v-for="(slide, i) in slides"
            :key="i"
            :image="slide.image">
          <template v-slot:content>

            <!--        <v-col align="center" class="mx-auto mt-16">-->
            <!--          <v-card width="600" color="rgb(0, 0, 0, 0.6)" dark >-->
            <!--            <v-card-text>-->
            <!--              <p class="display-1 font-weight-bold" > {{ slide.title }}</p>-->
            <!--              <h1>{{ slide.content }} </h1>-->
            <!--              <v-btn class="mt-4" :to="slide.to" color="blue" dark>more informations</v-btn>-->
            <!--            </v-card-text>-->
            <!--          </v-card>-->

            <!--        </v-col>-->
          </template>
        </vueper-slide>
      </vueper-slides>
    </v-container>

    <v-card class="blue--text grey lighten-1 ma-5">
      <v-card-title>
        <p>...More about my 3D - Printing - Hobby</p>
      </v-card-title>
      <v-card-text>
        <p>
          Angefangen habe ich mit dem Drucken gegen Ende des Jahres 2019.
        </p>
        <p>
          Mein Drucker:
        </p>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
  name: "3DPrinting",
  components: { VueperSlides, VueperSlide },
  data: () => ({
    slides: [
      {
        id: 1,
        content: 'My little printing on demand hobby',
        image: require('@/assets/Projects/3dDruck/main.jpeg'),
      },
      {
        id: 2,
        content: 'A creation from overlapping technologies',
        image: require('@/assets/Projects/ArduinoUnd3DDruck/main.jpeg'),
      },
    ]
  }),

}
</script>

<style scoped>

</style>