<script setup>
import { ref } from "vue";
let onhover = ref(false);
console.log(onhover.value);

</script>


<template>
  <div
    class="bg-grayish-blue w-screen h-screen flex justify-center items-center"
  >
    <div
      class="bg-light-grayish-blue flex xs:flex-col lg:flex-row rounded-xl overflow-hidden lg:w-[50rem] lg:h-72 xs:w-[90%] xs:h-[65%] shadow-md"
    >
      <img
        class="xs:w-full xs:h-1/3 lg:h-full lg:w-1/3 object-fill"
        src="https://github.com/Myudro33/article-preview-component/blob/main/src/assets/drawers.jpg?raw=true"
        alt="drawers"
      />
      <div class="flex flex-col xs:w-full xs:h-2/3 lg:w-2/3 lg:h-full p-8">
        <h1
          class="xs:text-lg lg:text-[1.6rem] text-dark-grayish-blue font-extrabold"
        >
          Shift the overall lock and feel by adding these wonderful touches to
          furniture in your home
        </h1>
        <p class="text-dark-grayish-blue font-medium text-base mt-2">
          Ever been in a room and felt like something was missing? Perhaps it
          felt slightlu bare and uninviting. i've got some simple tips to help
          you make any room complete.
        </p>
        <div class="mt-4 flex justify-between items-center w-full">
          <div class="flex items-center">
            <img
              class="w-10 h-10 rounded-full"
              src="https://github.com/Myudro33/article-preview-component/blob/main/src/assets/avatar-michelle.jpg?raw=true"
              alt="avatar"
            />
            <div class="flex flex-col ml-2">
              <h1 class="text-dark-grayish-blue font-bold">
                Michelle Appleton
              </h1>
              <p class="text-dark-grayish-blue font-medium">28 Jun 2020</p>
            </div>
          </div>
          <div
            @mouseenter="onhover = true"
            @mouseleave="onhover=false"
            class="w-14 h-full flex justify-center items-center"
          >
            <img class="hover:bg-dark-grayish-blue w-6 h-6 p-[5px] rounded-full"
            @mouseenter="onhover = true"
              src="https://raw.githubusercontent.com/Myudro33/article-preview-component/e31560e276c7b1e47c80368efbce7829d7842789/src/assets/icon-share.svg"
              alt="share"
            />
          </div>
          <div
            v-if="onhover"
            @mouseenter="onhover = true"
            class="w-52 h-20 absolute -translate-y-10 xs:right-0 lg:right-[22rem] flex flex-col items-center"
          >
            <div
              class="bg-dark-grayish-blue w-full h-14 rounded-xl p-2 flex items-center"
            >
              <h1 class="tracking-widest text-light-grayish-blue">SHARE</h1>
              <img
                class="ml-4 cursor-pointer"
                src="https://raw.githubusercontent.com/Myudro33/article-preview-component/a0f3d27544a6fd385c4a2bf7cdb77e54d18f1e55/src/assets/icon-facebook.svg"
                alt=""
              />
              <img
                class="ml-4 cursor-pointer"
                src="https://raw.githubusercontent.com/Myudro33/article-preview-component/a0f3d27544a6fd385c4a2bf7cdb77e54d18f1e55/src/assets/icon-twitter.svg"
                alt=""
              />
              <img
                class="ml-4 cursor-pointer"
                src="https://raw.githubusercontent.com/Myudro33/article-preview-component/a0f3d27544a6fd385c4a2bf7cdb77e54d18f1e55/src/assets/icon-pinterest.svg"
                alt=""
              />
            </div>
            <div
              class="w-5 h-5 rotate-45 -translate-y-3 bg-dark-grayish-blue"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
