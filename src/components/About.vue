<template>
  <div class="content flex-row">
    <div
      class="g grid grid-cols-5 gap-4 float-right overflow-auto justify-items-center h-full w-3/4 pt-4"
    >
      <div
        class="flex flex-col flex-auto flex-nowrap h-auto w-sv justify-center"
        v-for="(v, index) in series"
        :key="index"
      >
        <div
          @click="toVideo(v.video_id)"
          class="card w-sv h-sv mx-auto rounded transform ease-in-out duration-300 hover:scale-110"
        >
          <div
            class="card_cover rounded bg-gradient-to-bl from-gray-400 to-gray-900 cursor-pointer"
            :style="{ backgroundImage: 'url(' + v.video_img + ')' }"
          ></div>
        </div>
        <div
          class="flex flex-row flex-auto flex-nowrap w-sv space-x-2 mt-5 font-serif justify-center text-center h-auto"
        >
          <p
            @click="toVideo(v.video_id)"
            class="flex-auto text-xl text-gray-400 tracking-widest hover:text-blue-400 cursor-pointer truncate text-right"
          >
            {{ v.name_cn }}
          </p>
          <strong class="flex-auto text-red-500 text-xl font-bold text-left">{{
            v.score
          }}</strong>
        </div>
      </div>
    </div>
    <div class="h-full w-0.5 border-r-2 border-dashed border-gray-400"></div>
    <div class="flex flex-col flex-auto flex-nowrap space-y-4 h-auto w-1/4">
      <div
        class="h-10 justify-center font-twi text-2xl font-semibold tracking-widest text-green-400 text-left pl-3 border-b-2 border-dashed border-gray-400"
      >
        Recommend
      </div>
      <div class="g grid grid-cols-3 gap-4 justify-items-center h-72 mx-auto">
        <div
          class="flex flex-col flex-auto flex-nowrap justify-center w-sr"
          v-for="(v, index) in series"
          :key="index"
        >
          <div
            @click="toVideo(v.video_id)"
            class="card w-sr h-sr mx-auto rounded"
          >
            <div
              class="card_cover rounded bg-gradient-to-bl from-gray-400 to-gray-900 cursor-pointer"
              :style="{ backgroundImage: 'url(' + v.video_img + ')' }"
            ></div>
          </div>
          <div
            class="flex flex-row flex-auto flex-nowrap w-sr space-x-1 mt-1 font-serif justify-center text-center"
          >
            <p
              @click="toVideo(v.video_id)"
              class="flex-auto text-base tracking-widest text-gray-400 hover:text-blue-400 cursor-pointer truncate text-right"
            >
              {{ v.name_cn }}
            </p>
            <strong
              class="flex-auto text-base font-bold text-red-500 text-left"
              >{{ v.score }}</strong
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "about",
  data() {
    return {
      series: [
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿asdasdasdasdads",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
        {
          video_id: "1",
          video_img:
            "https://bit-images.bj.bcebos.com/bit-new/file/20210116/fuwk.jpg",
          name_cn: "嘿嘿嘿",
          name_en: "asdasd",
          score: "9.2",
        },
      ],
    };
  },
  methods: {
    toVideo(vid: string) {
      this.$router.push({
        path: "/series/video",
        query: { vid: vid },
      });
    },
  },
  props:['list']
});
</script>

<style scoped>
.g::-webkit-scrollbar {
  width: 10px;
  color: #2d333b;
}
</style>