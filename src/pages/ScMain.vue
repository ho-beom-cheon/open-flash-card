<template>
  <body>
  <div class="q-pa-md row items-start q-gutter-md">

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h5 q-mb-xs">경제</div>
        <div class="row no-wrap items-center" @click="onclick">
          <q-rating size="18px" v-model="stars" :max="5" color="primary" />
          <span class="text-caption text-grey q-ml-sm">{{ stars[1] }} (551)</span>
        </div>
      </q-card-section>

      <img src="http://pimg.daara.co.kr/kidd/photo/2016/09/30/thumbs/thumb_520390_1475224904_40.jpg">
    </q-card>

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h5 q-mb-xs">문화</div>
        <div class="row no-wrap items-center">
          <q-rating size="18px" v-model="stars" :max="5" color="primary" />
          <span class="text-caption text-grey q-ml-sm">{{ stars[2] }} (551)</span>
        </div>
      </q-card-section>

      <img src="https://arte365.kr/wp-content/uploads/2017/07/170724_column_thum.jpg">
    </q-card>

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h5 q-mb-xs">과학</div>
        <div class="row no-wrap items-center">
          <q-rating size="18px" v-model="stars" :max="5" color="primary" />
          <span class="text-caption text-grey q-ml-sm">{{ stars[3] }} (551)</span>
        </div>
      </q-card-section>

      <img src="https://post-phinf.pstatic.net/MjAxNzA0MjFfNjIg/MDAxNDkyNzUwMDI3NDQ1.Dg87-LjqpfzEa5z6kVRs-DJ7OoyEC-lcV2bk1PA7KFcg.KoREpSfJO7JXSWU4Ie2j0Hz5kX4nJyw-z4FKCJopUAcg.JPEG/%EA%B3%BC%ED%95%99%EC%9D%98_%EB%82%A0.jpg?type=w1200">
    </q-card>

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h5 q-mb-xs">IT</div>
        <div class="row no-wrap items-center">
          <q-rating size="18px" v-model="stars" :max="5" color="primary" />
          <span class="text-caption text-grey q-ml-sm">{{ stars[4] }} (551)</span>
        </div>
      </q-card-section>

      <img src="https://mblogthumb-phinf.pstatic.net/MjAxOTA3MDVfMjc0/MDAxNTYyMjk0OTgzODUw.HfEwtkED2NCURwxy1EKNCPwys7lMct3bP65VWkKICeAg.0vVtHt-KwvdT2p6A1GFlWGZW60n0uKyz6PNYGjMMY0Ug.JPEG.naverschool/IT-IoT-ICT-GettyImages-1159121061.jpg?type=w800">
    </q-card>

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h5 q-mb-xs">세계</div>
        <div class="row no-wrap items-center">
          <q-rating size="18px" v-model="stars" :max="5" color="primary" />
          <span class="text-caption text-grey q-ml-sm">{{ stars[5] }} (551)</span>
        </div>
      </q-card-section>

      <img src="https://cwcontent.asiae.co.kr/asiaresize/219/2020040610425861184_1586137378.jpg">
    </q-card>

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h5 q-mb-xs">신조어</div>
        <div class="row no-wrap items-center">
          <q-rating size="18px" v-model="stars" :max="5" color="primary" />
          <span class="text-caption text-grey q-ml-sm">{{ stars[5] }} (551)</span>
        </div>
      </q-card-section>

      <img src="data:image/jpeg;base64,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">
    </q-card>
  </div>
  </body>
</template>

<script>
import { ref } from 'vue'

export default {
  props: {
    title: String
  },
  setup () {
    return {
      starRate : ref(5),
      stars: ref([5,3,2,1,4,2]),
    }
  }
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width:  510px
</style>
