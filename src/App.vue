<template>
  <div>
    <header>
      <div class="logo-container">
        <img src="@/assets/images/logo.png" alt="logo" />
      </div>
      <div class="image-container">
        <img alt="shape" src="@/assets/images/shape.png" />
      </div>
      <div class="content">
        <div class="text-container">
          <span class="first-text">¿Necesitas ayuda?</span>
          <br />
          <span class="second-text"
            >Pide servicios mediante nuestra app, son&nbsp;</span
          >
          <vue-typer
            :text="['confiables', 'de calidad', 'seguros', 'rápidos']"
          ></vue-typer>
        </div>
        <div class="icons-dock">
          <div class="icon-container">
            <i class="fab fa-apple"></i>
          </div>
          <a
            href="https://serconexion-web.s3.us-east-2.amazonaws.com/app-x86_64-release.apk"
            download
          >
            <div class="icon-container">
              <i class="fab fa-android"></i>
            </div>
          </a>
        </div>
      </div>
      <div class="device">
        <img src="@/assets/images/device.png" alt="device" />
      </div>
    </header>
  </div>
</template>

<script>
import { VueTyper } from "vue-typer";

export default {
  name: "App",
  components: {
    vueTyper: VueTyper
  }
};
</script>

<style lang="scss">
header {
  position: relative;
  height: 100vh;
}

.logo-container {
  position: absolute;
  width: 4vw;
  top: 3vw;
  left: 10vw;

  img {
    width: 100%;
  }
}

.image-container {
  position: absolute;
  z-index: -1;
  right: 0;
  width: 70%;

  img {
    width: 100%;
  }
}

.content {
  position: relative;
  top: 50%;
  left: 10vw;
  transform: translateY(-50%);
  width: 35vw;

  .text-container {
    .first-text {
      font-size: 3.4vw;
      font-weight: bolder;
    }

    .second-text {
      font-size: 2.4vw;
      font-weight: 300;
    }
  }

  .icons-dock {
    display: flex;

    .icon-container {
      padding: 1.5vw;
      background-color: #2c3a47;
      color: white;
      border-radius: 1vw;
      margin-right: 1vw;
      margin-top: 1vw;
      cursor: pointer;
      transition-property: all;
      transition-duration: 300ms;

      &:hover {
        background-color: #fd7272;
        transform: scale(1.2);
      }

      i {
        font-size: 1.2vw;
      }
    }
  }
}

.device {
  position: absolute;

  right: 8vw;
  top: 50%;
  transform: translateY(-50%);

  img {
    width: 40vw;
  }
}

.vue-typer {
  font-size: 2.4vw;
  font-weight: 300;

  .custom.char.selected {
    background-color: #2c3a47;
    color: #ffffff;
  }

  .custom.caret {
    width: 1rem;
    background-color: #fd7272;
  }
}
</style>
