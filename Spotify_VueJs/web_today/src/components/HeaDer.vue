<template>
  <div
    v-on:click="counter.Show_delete = 0"
    class="flex flex-col fixed z-40 bg-black dark:bg-slate-900 min-h-screen w-[250px] drop-shadow-md shrink-0"
  >
    <div class="flex pl-7 py-6 w-full">
      <router-link
        to="/"
        class="flex items-center gap-2 w-full"
        v-on:click="counter.Show_Search = 1"
      >
        <img class="w-[60px] h-[60px]" src="@/assets/posterMR.png" />
        <h1 class="text-[25px] font-bold text-gray-200">MR</h1>
        <!-- <svg viewBox="0 0 1134 340" class="w-[131px]">
                    <title>Spotify</title>
                    <path class="fill-white" fill="currentColor" d="M8 171c0 92 76 168 168 168s168-76 168-168S268 4 176 4 8 79 8 171zm230 78c-39-24-89-30-147-17-14 2-16-18-4-20 64-15 118-8 162 19 11 7 0 24-11 18zm17-45c-45-28-114-36-167-20-17 5-23-21-7-25 61-18 136-9 188 23 14 9 0 31-14 22zM80 133c-17 6-28-23-9-30 59-18 159-15 221 22 17 9 1 37-17 27-54-32-144-35-195-19zm379 91c-17 0-33-6-47-20-1 0-1 1-1 1l-16 19c-1 1-1 2 0 3 18 16 40 24 64 24 34 0 55-19 55-47 0-24-15-37-50-46-29-7-34-12-34-22s10-16 23-16 25 5 39 15c0 0 1 1 2 1s1-1 1-1l14-20c1-1 1-1 0-2-16-13-35-20-56-20-31 0-53 19-53 46 0 29 20 38 52 46 28 6 32 12 32 22 0 11-10 17-25 17zm95-77v-13c0-1-1-2-2-2h-26c-1 0-2 1-2 2v147c0 1 1 2 2 2h26c1 0 2-1 2-2v-46c10 11 21 16 36 16 27 0 54-21 54-61s-27-60-54-60c-15 0-26 5-36 17zm30 78c-18 0-31-15-31-35s13-34 31-34 30 14 30 34-12 35-30 35zm68-34c0 34 27 60 62 60s62-27 62-61-26-60-61-60-63 27-63 61zm30-1c0-20 13-34 32-34s33 15 33 35-13 34-32 34-33-15-33-35zm140-58v-29c0-1 0-2-1-2h-26c-1 0-2 1-2 2v29h-13c-1 0-2 1-2 2v22c0 1 1 2 2 2h13v58c0 23 11 35 34 35 9 0 18-2 25-6 1 0 1-1 1-2v-21c0-1 0-2-1-2h-2c-5 3-11 4-16 4-8 0-12-4-12-12v-54h30c1 0 2-1 2-2v-22c0-1-1-2-2-2h-30zm129-3c0-11 4-15 13-15 5 0 10 0 15 2h1s1-1 1-2V93c0-1 0-2-1-2-5-2-12-3-22-3-24 0-36 14-36 39v5h-13c-1 0-2 1-2 2v22c0 1 1 2 2 2h13v89c0 1 1 2 2 2h26c1 0 1-1 1-2v-89h25l37 89c-4 9-8 11-14 11-5 0-10-1-15-4h-1l-1 1-9 19c0 1 0 3 1 3 9 5 17 7 27 7 19 0 30-9 39-33l45-116v-2c0-1-1-1-2-1h-27c-1 0-1 1-1 2l-28 78-30-78c0-1-1-2-2-2h-44v-3zm-83 3c-1 0-2 1-2 2v113c0 1 1 2 2 2h26c1 0 1-1 1-2V134c0-1 0-2-1-2h-26zm-6-33c0 10 9 19 19 19s18-9 18-19-8-18-18-18-19 8-19 18zm245 69c10 0 19-8 19-18s-9-18-19-18-18 8-18 18 8 18 18 18zm0-34c9 0 17 7 17 16s-8 16-17 16-16-7-16-16 7-16 16-16zm4 18c3-1 5-3 5-6 0-4-4-6-8-6h-8v19h4v-6h4l4 6h5zm-3-9c2 0 4 1 4 3s-2 3-4 3h-4v-6h4z"></path>
                </svg> -->
      </router-link>
    </div>
    <div class="flex flex-col px-4 py-4 justify-between w-full font-bold">
      <div class="flex flex-col text-slate-100 px-3 mt-2 gap-4 text-[19px]">
        <router-link
          to="/"
          class="flex items-center gap-2 hover:ml-2 hover:text-yellow-500 cursor-pointer duration-100"
          v-bind:class="{
            'text-yellow-500': counter.Path_Route.path == '/SeaFood',
          }"
        >
          <svg
            role="img"
            height="24"
            width="24"
            aria-hidden="true"
            class="Svg-sc-ytk21e-0 uPxdw home-icon fill-gray-300"
            viewBox="0 0 24 24"
            data-encore-id="icon"
          >
            <path
              d="M12.5 3.247a1 1 0 0 0-1 0L4 7.577V20h4.5v-6a1 1 0 0 1 1-1h5a1 1 0 0 1 1 1v6H20V7.577l-7.5-4.33zm-2-1.732a3 3 0 0 1 3 0l7.5 4.33a2 2 0 0 1 1 1.732V21a1 1 0 0 1-1 1h-6.5a1 1 0 0 1-1-1v-6h-3v6a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V7.577a2 2 0 0 1 1-1.732l7.5-4.33z"
            ></path>
          </svg>
          <h1
            :class="{ 'text-white': counter.Path_Route.path == '/' }"
            class="text-[13px] ml-2 text-gray-300 font-medium"
          >
            Trang chủ
          </h1>
        </router-link>
        <router-link
          to="/Search"
          v-on:click="counter.Search_Song = ''"
          class="flex items-center gap-2 hover:ml-2 hover:text-yellow-500 cursor-pointer duration-100"
          v-bind:class="{
            'text-yellow-500': counter.Path_Route.path == '/WaterFood',
          }"
        >
          <svg
            role="img"
            height="24"
            width="24"
            aria-hidden="true"
            class="Svg-sc-ytk21e-0 uPxdw search-active-icon fill-gray-300"
            viewBox="0 0 24 24"
            data-encore-id="icon"
          >
            <path
              d="M15.356 10.558c0 2.623-2.16 4.75-4.823 4.75-2.664 0-4.824-2.127-4.824-4.75s2.16-4.75 4.824-4.75c2.664 0 4.823 2.127 4.823 4.75z"
            ></path>
            <path
              d="M1.126 10.558c0-5.14 4.226-9.28 9.407-9.28 5.18 0 9.407 4.14 9.407 9.28a9.157 9.157 0 0 1-2.077 5.816l4.344 4.344a1 1 0 0 1-1.414 1.414l-4.353-4.353a9.454 9.454 0 0 1-5.907 2.058c-5.18 0-9.407-4.14-9.407-9.28zm9.407-7.28c-4.105 0-7.407 3.274-7.407 7.28s3.302 7.279 7.407 7.279 7.407-3.273 7.407-7.28c0-4.005-3.302-7.278-7.407-7.278z"
            ></path>
          </svg>
          <h1
            :class="{ 'text-white': counter.Path_Route.path == '/Search' }"
            class="text-[13px] ml-2 text-gray-300 font-medium"
          >
            Tìm kiếm
          </h1>
        </router-link>
        <router-link
          to="/MyLibary"
          class="flex items-center gap-2 hover:ml-2 hover:text-yellow-500 cursor-pointer duration-100"
          v-bind:class="{
            'text-yellow-500': counter.Path_Route.path == '/Cachloroathite',
          }"
        >
          <svg
            role="img"
            height="24"
            width="24"
            aria-hidden="true"
            class="Svg-sc-ytk21e-0 uPxdw collection-icon fill-gray-300"
            viewBox="0 0 24 24"
            data-encore-id="icon"
          >
            <path
              d="M14.5 2.134a1 1 0 0 1 1 0l6 3.464a1 1 0 0 1 .5.866V21a1 1 0 0 1-1 1h-6a1 1 0 0 1-1-1V3a1 1 0 0 1 .5-.866zM16 4.732V20h4V7.041l-4-2.309zM3 22a1 1 0 0 1-1-1V3a1 1 0 0 1 2 0v18a1 1 0 0 1-1 1zm6 0a1 1 0 0 1-1-1V3a1 1 0 0 1 2 0v18a1 1 0 0 1-1 1z"
            ></path>
          </svg>
          <h1
            :class="{ 'text-white': counter.Path_Route.path == '/MyLibary' }"
            class="text-[13px] ml-2 text-gray-300 font-medium"
          >
            Thư viện của tôi
          </h1>
        </router-link>
        <!-- <div  class="flex items-center gap-2 hover:ml-2 hover:text-yellow-500 cursor-pointer duration-100" -->
        <a
          href="http://localhost:8501"
          target="blank_"
          class="flex text-[19px] text-gray-300 font-medium items-center hover:ml-2 cursor-pointer duration-100 gap-4"
          ><font-awesome-icon icon="fa-solid fa-robot" />
          <h1 class="text-[13px]">Chat Bot</h1>
        </a>
        <!-- </div> -->
      </div>
    </div>
    <div class="flex flex-col px-4 py-4 justify-between w-full font-bold">
      <div class="flex flex-col text-slate-100 px-3 mt-2 gap-4 text-[19px]">
        <router-link
          to="/Play-list"
          v-on:click="
            counter.Show_bang_DT = 2;
            counter.Search_Song = '';
          "
          class="flex items-center gap-2 hover:ml-2 hover:text-yellow-500 cursor-pointer duration-100"
          v-bind:class="{
            'text-yellow-500': counter.Path_Route.path == '/SeaFood',
          }"
        >
          <div
            class="flex items-center justify-center bg-gray-300 rounded-[2px] h-[24px] w-[24px]"
          >
            <svg
              role="img"
              height="12"
              width="12"
              aria-hidden="true"
              viewBox="0 0 16 16"
              data-encore-id="icon"
              class="Svg-sc-ytk21e-0 uPxdw"
            >
              <path
                d="M15.25 8a.75.75 0 0 1-.75.75H8.75v5.75a.75.75 0 0 1-1.5 0V8.75H1.5a.75.75 0 0 1 0-1.5h5.75V1.5a.75.75 0 0 1 1.5 0v5.75h5.75a.75.75 0 0 1 .75.75z"
              ></path>
            </svg>
          </div>
          <h1
            :class="{ 'text-white': counter.Path_Route.path == '/Play-list' }"
            class="text-[13px] ml-2 text-gray-300 font-medium"
          >
            Tạo Danh sách Phát
          </h1>
        </router-link>
        <router-link
          to="/Love-Song"
          class="flex items-center gap-2 hover:ml-2 hover:text-yellow-500 cursor-pointer duration-100 border-b-[1px] border-neutral-700 pb-5"
          v-bind:class="{
            'text-yellow-500': counter.Path_Route.path == '/WaterFood',
          }"
        >
          <div
            class="flex items-center justify-center bg-gradient-to-t from-violet-400 to-violet-500 rounded-[2px] h-[24px] w-[24px]"
          >
            <svg
              role="img"
              height="12"
              width="12"
              aria-hidden="true"
              viewBox="0 0 16 16"
              data-encore-id="icon"
              class="Svg-sc-ytk21e-0 uPxdw fill-gray-300"
            >
              <path
                d="M15.724 4.22A4.313 4.313 0 0 0 12.192.814a4.269 4.269 0 0 0-3.622 1.13.837.837 0 0 1-1.14 0 4.272 4.272 0 0 0-6.21 5.855l5.916 7.05a1.128 1.128 0 0 0 1.727 0l5.916-7.05a4.228 4.228 0 0 0 .945-3.577z"
              ></path>
            </svg>
          </div>
          <h1
            :class="{ 'text-white': counter.Path_Route.path == '/Love-Song' }"
            class="text-[13px] ml-2 text-gray-300 font-medium"
          >
            Bài hát yêu thích
          </h1>
        </router-link>
      </div>
    </div>
    <div class="flex flex-col justify-center">
      <div
        class="flex pr-5"
        v-for="(i, index) in counter.Get_song_play_list.data"
      >
        <div
          v-on:click="
            counter.show_bang_DSP = i.id;
            counter.show_bang_DSPN = index;
            counter.name_show_bang_DSPN = i.id;
            counter.Show_deletete = 0;
          "
          v-on:contextmenu.prevent="
            counter.Show_delete = i.id;
            counter.name_delete_play_list = i.id;
          "
          :class="{ 'text-white': counter.show_bang_DSP == i.id }"
          class="text-gray-300 text-[13px] px-4 py-2 ml-2 justify-between w-full font-medium cursor-pointer"
        >
          Danh sách Phát # {{ i.name }}
        </div>
        <div
          v-show="counter.Show_delete == i.id"
          v-on:click="delete_listt()"
          class="bg-gray-900 rounded px-3 py-1 w-[100px] h-[30px] text-gray-100 text-[13px] cursor-pointer"
        >
          Xóa
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { useCounterStore } from "@/stores/counter";
import axios from "axios";
import VueCookies from "vue-cookies";

export default {
  setup() {
    const counter = useCounterStore();
    return { counter };
  },
  mounted: function () {
    // this.counter.get_song_play_list();
  },
  // destroyed () {
  // document.body.classList.remove('overflow-hidden')
  // },
  methods: {
    async set_play_listt() {
      await this.counter.get_song_play_list();
      await this.counter.set_play_list(
        this.counter.Get_song_play_list.data.length + 1
      );
      await this.counter.get_song_play_list();
    },
    async delete_listt() {
      await this.counter.delete_play_list();
      await this.counter.get_song_play_list();
    },
  },
};
</script>

<!-- <style v-if="counter.Open_Scroll==2">
  body {
   overflow: default;
  }
</style> -->

<!-- <style v-if="true">
  body {
   overflow: hidden;
  }
</style> -->
