<script>
import Button from "../components/reusable/Button.vue";
export default {
  scrollToTop: true,
  components: { Button },
};
</script>

<template>
  <div class="flex flex-col items-center font-phu-du">
    <div class="mt-7 h-14 w-14"><img class="w-full h-auto" alt="home-logo" src="~/static/img/1x/home_logo.png"></div>
    <img class="mx-5 scale-90 image-header" src="~/static/img/earth_in_home.png">

    <h3 class="text-blue1 font-livic-bold font-black leading-10 text-lg"> <span class="py-2 px-1">GIẢM "ĐIỂM NHỰA"
        -
        TĂNG ĐIỂM XANH</span> </h3>
    <div class="font-livic text-blue1 w-80 text-center text-base leading-1">Mọi vật phẩm bạn cầm tay trong chuyến du lịch
      của mình đều ảnh hưởng ít nhiều tới môi trường xung quanh. Hãy cùng tra cứu “mức độ ảnh hưởng môi trường” của nhựa
      dùng một lần và chuẩn bị hành lý “xanh” cho một chuyến đi gắn kết với thiên nhiên nhé.
    </div>

    <button @click="routeTo('/soando')"
      class="bg-button w-full bg-center h-12 bg-no-repeat bg-contain mt-10 mb-3 mx-2">
      <span class="py-2 px1 text-white1 normal-case font-black tracking-wide">TRA CỨU NHỰA DÙNG MỘT LẦN</span>

    </button>
    <button @click="routeTo('/valimau')"
      class="bg-button-border w-full bg-center h-12 bg-no-repeat bg-contain mb-3">
      <span class="text-blue1 tracking-wide normal-case font-black">CẨM NANG DU LỊCH XANH</span>
    </button>
    <button @click="routeTo('/camket')"
      class="bg-button-border w-full bg-center h-12 bg-no-repeat bg-contain mb-5">
      <span class="text-blue1 tracking-wide normal-case font-black">TÔI CAM KẾT "KIÊNG NHỰA"</span>
    </button>
    <iframe class="mx-auto" width="375px" height="210px"
      src="https://www.youtube.com/embed/rvBz2wLoDOI?si=MZD0jCJs_yeOPNDo" title="YouTube video player" frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen></iframe>

    <div class="bg-cyan1 flex flex-col items-center w-full py-5 px-1">
      <div class="font-livic-bold font-bold text-white1 w-80 text-center text-on-mobile">
        <span class="text-xl leading-1 px-1 py-2 font-black">“DETOX” TRÁI ĐẤT KHỎI RÁC NHỰA DÙNG MỘT LẦN</span>
      </div>
      <!-- <div class="font-phu-du font-bold text-white1 w-80 text-center text-on-mobile">
        <span class="text-xl leading-1 px-1 py-2 font-black">NHỰA KHÔNG XẤU,</span> <br>
        <span class="text-xl leading-1 px-1 py-2 font-black">CHO TỚI KHI CHÚNG TA</span> <br>
        <span class="text-xl leading-1 px-1 py-2 font-black">DÙNG NHỰA THIẾU TRÁCH NHIỆM</span>
      </div>
      <div class="font-phu-du font-bold text-white1 text-center text-on-desktop">
        <span class="text-xl leading-1 px-1 py-2 font-black">NHỰA KHÔNG XẤU, CHO TỚI KHI CHÚNG TA DÙNG NHỰA THIẾU TRÁCH
          NHIỆM</span>
      </div> -->
      <div class="font-livic text-blue1 text-center font-bold mx-6 mt-3 text-base">
        <div>Website “Kiêng Nhựa" giúp bạn định lượng mức độ ảnh hưởng đến môi trường của các sản phẩm đồ nhựa sử dụng một
          lần thông dụng nhất, để từ đó điều chỉnh hành vi lựa chọn và sử dụng đồ nhựa “xanh” hơn, và có trách nhiệm với
          môi trường hơn trong mỗi chuyến du lịch của mình.
        </div>
        <div class="mt-2">
          Website được tài trợ trong phạm vi dự án “Giảm thiểu Rác thải nhựa đại dương tại Việt Nam” do Cục Biển và Hải
          đảo Việt Nam phối hợp với Tổ chức Quốc tế về Bảo tồn thiên nhiên WWF triển khai.
        </div>
        <div class="mt-2">Cùng học cách chuẩn bị hành trang du lịch “xanh" qua hướng dẫn dưới đây.</div>
      </div>
      <button @click="routeTo('/valimau')"
        class="bg-button-border-white w-full bg-center h-12 bg-no-repeat bg-contain mb-3 mt-5">
        <span class="text-blue1 tracking-wide normal-case font-black">CẨM NANG DU LỊCH XANH</span>
      </button>
    </div>

  </div>
</template>

<script>
// import { getIdFromURL } from "vue-youtube-embed";
// let videoId = getIdFromURL("https://www.youtube.com/watch?v=24C8r8JupYY");

export default {
  name: 'Home',
  methods: {
    routeTo(path) {
      this.$router.push(path);
    },
    toggleInfo(value) {
      this.openInfo = !!value
    },
    toggleMenu(value) {
      this.openMenu = !!value
    }
  }
}
</script>

<style scoped>
.mt-40p {
  margin-top: 40%;
}

.w-45p {
  width: 45%;
}

.w-80p {
  width: 80%;
}

.w-85p {
  width: 85%;
}

.w-150px {
  width: 150px;
}

.top-2px {
  top: 2px;
}

.image-header {
  width: 40vh;
}

@media screen and (max-width: 768px) {
  .text-on-mobile {
    display: block;
  }

  .text-on-desktop {
    display: none;
  }
}

.text-on-mobile {
  display: none;
}

.text-on-desktop {
  display: block;
}
button {
  font-family: 'LivvicBold' !important;
}
@media screen and (max-width: 768px) {
  .text-on-mobile {
    display: block;
  }

  .text-on-desktop {
    display: none;
  }
}
</style>
