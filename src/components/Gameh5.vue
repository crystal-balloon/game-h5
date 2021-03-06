<template>
  <div class="h5-root">
    <div class="page-header">
      <img class="layer-20" />
      <img class="layer-19" />
      <img class="aisi" />
      <img class="lufei" />
      <img class="sabo" />
      <img class="head-actor" />
      <img class="b small-icon" />
      <img class="c small-icon" />
      <img class="d small-icon" />
      <img class="doc" />
      <img class="short-copyright" />
      <img class="rect-2-7" />
    </div>

    <div class="page-body">
      <img class="rect-1" />
      <img class="group-10" />
      <img class="my-prize-100" />
      <img class="layer-18" />
      <img class="draw-once" />
      <img class="layer-18-copy" />
      <img class="share-to-friends" />
      <img class="daily-login-prize" />
      <img class="draw-label" />
      <img class="rect-3-4" />
      <img class="rect-2-9" />
    </div>
    <div class="page-footer">
      <img class="rect-1-3" />
      <img class="rect-3-8" />
      <img class="lucky-value" />
      <img class="share" />
    </div>
  </div>
</template>

<script>
import { idImageMapping } from "./utils";

export default {
  name: "Gameh5",
  mounted() {
    Object.keys(idImageMapping).forEach((className) => {
      const dom = document.querySelector(`.${className}`);
      if (dom) {
        if (dom instanceof Image) {
          const imagePath = `./res/${idImageMapping[className]}.png`;
          dom.src = imagePath;
        } else {
          const bgPath = `url(./res/${idImageMapping[className]}.png)`;
          dom.style.backgroundImage = bgPath;
          dom.style.backgroundSize = "100% 100%";
        }
      }
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.h5-root {
  width: 100%;

  *div {
    background-size: 100% 100%;
  }

  .page-header {
    position: relative;
    img {
      position: absolute;
      top: 0;
      width: 100%;
    }
    .layer-19 {
      position: absolute;
      width: 100%;
      top: 32%;
    }
    .layer-20 {
      width: 100%;
      left: 0;
      top: 94%;
    }
    .head-actor {
      width: 100%;
      position: relative;
    }
    .lufei {
      margin: auto;
      width: 60%;
      height: 100%;
      left: 20%;
    }
    .aisi,
    .sabo {
      width: 39%;
      height: 100%;
    }
    .sabo {
      right: 0;
    }
    .b,
    .c,
    .d {
      width: 7%;
      height: 6%;
    }
    .b {
      left: 54%;
      top: 27%;
    }
    .c {
      top: 57%;
      left: 13%;
    }
    .d {
      top: 54%;
      left: 83%;
    }
    .doc {
      $width: 72%;
      width: $width;
      bottom: 1%;
      top: unset;
      left: calc((100% - #{$width}) / 2);
    }
    .short-copyright {
      bottom: 0;
      left: 0;
      top: unset;
      width: 15%;
    }
    .rect-2-7 {
      right: 0;
      bottom: 0;
      top: unset;
      width: 5%;
      transform: translateY(50%);
    }
  }

  .page-body {
    position: relative;
    $left: 5%;

    img {
      position: absolute;
      top: 0;
      left: $left;
    }
    .rect-1 {
      position: relative;
      width: calc(100% - #{$left});
    }

    .group-10 {
      $pd-left: 3%;
      left: $left + $pd-left;
      width: calc(100% - #{$left + $pd-left * 2});
      top: $left + $pd-left - 3%;
    }

    .my-prize-100 {
      top: 35%;
      left: 38%;
      width: 30%;
    }
    .layer-18 {
      top: 40%;
      left: 37%;
      width: 32%;
      // z-index: 1;
    }
    .draw-once {
      top: 42%;
      left: 44%;
      width: 18%;
      // z-index: 2;
    }
    .layer-18-copy {
      top: 52%;
      left: 37%;
      width: 32%;
    }
    .share-to-friends {
      top: 54%;
      left: 41%;
      width: 24%;
    }
    .daily-login-prize {
      top: 65%;
      left: 40%;
      width: 25%;
    }
    .draw-label {
      width: 74%;
      top: 6.6%;
      left: 7.8%;
    }
    .rect-3-4 {
      top: 1%;
      left: 0;
      width: 2.5%;
    }
    .rect-2-9 {
      left: 5.5%;
      width: 43%;
      top: 1%;
    }
  }
  .page-footer {
    position: relative;
    .rect-1-3 {
      width: 97%;
      position: absolute;
      top: 3%;
    }
    .rect-3-8 {
      right: 0;
      position: absolute;
      top: 3.5%;
      width: 2.5%;
    }
    .lucky-value {
      top: 55%;
      left: 0;
      width: 97%;
      position: relative;
      margin-top: 3%;
    }
    .share {
      top: 33%;
      left: 0;
      width: 97%;
      position: absolute;
    }
  }
}
</style>
