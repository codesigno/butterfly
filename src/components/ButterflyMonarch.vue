<template>
  <div class="model">
    <model-gltf
      src="static/butterfly/butterfly.gltf"
      :backgroundAlpha="bgAlpha"
      :backgroundColor="bgColor"
    >
    </model-gltf>
    <div class="txt">
      <h1>beautiful butterfly</h1>
      <h2>3D</h2>
      <p>use mouse to rotate the butterfly</p>
    </div>
  </div>
</template>

<script>
import { ModelGltf } from "vue-3d-model";

export default {
  data() {
    return {
      bgColor: "#ff0",
      bgAlpha: 0.1,
    };
  },
  components: {
    ModelGltf,
  },
};
</script>

<style>
canvas {
  width: 95vw;
  height: 80vh;
  background-image: url("../assets/img/blooming-field.jpg");
  background-size: contain;
  background-repeat: no-repeat;
}
.model {
  width: 90vw;
  height: 95vh;
  display: flex;
  justify-content: center;
  align-items: center;
  /* flex-wrap: wrap; */
  position: absolute;
  top: 0;
  z-index: 9;
}
.txt {
  width: 18vw;
  padding: 0 1rem;
}
h2 {
  padding: 0.5rem 0;
}
.txt p {
  text-align: center;
}
</style>