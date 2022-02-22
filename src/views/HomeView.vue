<script>
import Granim from "granim";

export default {
  data: function () {
    return {
      message: "This would be so much cooler if I could get the logo example to work, lol",
    };
  },
  mounted() {
    var granimInstance = new Granim({
      element: "#canvas-image-blending",
      direction: "top-bottom",
      isPausedWhenNotInView: true,
      image: {
        source: "https://crowdink.com/wp-content/uploads/2017/04/thechive-tapiture-books.jpg",
        blendingMode: "multiply",
      },
      states: {
        "default-state": {
          gradients: [
            ["#29323c", "#485563"],
            ["#FF6B6B", "#556270"],
            ["#80d3fe", "#7ea0c4"],
            ["#f0ab51", "#eceba3"],
          ],
          transitionSpeed: 7000,
        },
      },
    });
    console.log("Granim Instance", granimInstance);
  },
};
</script>

<template>
  <div class="home">
    {{ message }}
  </div>
  <br />
  <div><canvas id="canvas-image-blending"></canvas></div>
</template>

<style>
#canvas-image {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
</style>
