<template>
  <div id="app">
    <!-- <Parallax></Parallax> -->

    <h1 class="text-center">Simple parallax</h1>
    <div class="parallax-effect-container">
      <div class="parallax-effect-image first"></div>
      <div class="parallax-effect-content">
        <h2 class="text-center invert">I'd like more simple CSS effects please</h2>
      </div>
    </div>
    <div class="parallax-effect-container">
      <div class="parallax-effect-image second"></div>
      <div class="parallax-effect-content">
        <h2 class="text-center invert">I'd like more simple CSS effects please</h2>
      </div>
    </div>
    <div class="parallax-effect-container">
      <div class="parallax-effect-image third"></div>
      <div class="parallax-effect-content-end">
        <h2 class="text-center invert">I'd like more simple CSS effects please</h2>
      </div>
    </div>
    <h1 class="text-center">Simple parallax</h1>
  </div>
</template>

<script>
// import Parallax from "./components/Parallax.vue";

export default {
  name: "App",
  components: {
    // Parallax
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Cabin");

* {
  margin: 0;
  padding: 0;
}
body {
  font-family: "Cabin", sans-serif;
  padding: 200px 0px;
  color: #545454;
}
a {
  color: inherit;
}
p {
  text-align: right;
  margin-bottom: 16px;
}
.first {
  background-image: url("./assets/1.png");
}
.second {
  background-image: url("./assets/2.png");
}
.third {
  background-image: url("./assets/3.png");
}

.parallax-effect-container {
  height: 100vh;
  overflow: hidden;
  display: block;
  background: black;

  position: relative;
  overflow: hidden;
}
.parallax-effect-content {
  position: absolute;
  display: block;
  max-width: 100%;
  top: 50%;
  left: 0;
  padding: 16px;
  width: 100%;
  transform-style: flat;
  transform: translate3d(0, -50%, 0);
}
.parallax-effect-content-end {
  
  display: block;
  max-width: 100%;
  height: 100vh;

  padding: 16px;
  width: 100%;
  transform-style: flat;
  transform: translate3d(0, -50%, 0);
}

.parallax-effect-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  bottom: 0;
  right: 0;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-attachment: fixed;
}

.text-center {
  text-align: center;
  font-size: 52px;
  margin-bottom: 22px;
  display: block;
  box-sizing: border-box;
  max-width: 100%;
}

.invert {
  color: white;
}
</style>
