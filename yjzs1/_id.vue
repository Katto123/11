<template>
  <div id="scene">
    <div class="t1" style="z-index: 8" data-depth="0.2">
      <img src="/yjzs/ch1.png" alt="" />
    </div>
    <div class="t2" style="z-index: 7" data-depth="0.7">
      <img src="/yjzs/ch2.png" alt="" />
    </div>
    <div class="t3" style="z-index: 6" data-depth="0.4">
      <img src="/yjzs/ch3.png" alt="" />
    </div>
    <div class="t4" style="z-index: 5" data-depth="0.3">
      <img src="/yjzs/ch4.png" alt="" />
    </div>
    <div class="t5" style="z-index: 4" data-depth="0.6">
      <img src="/yjzs/ch5.png" alt="" />
    </div>
    <div class="t6" style="z-index: 3" data-depth="0.9">
      <img src="/yjzs/ch6.png" alt="" />
    </div>
  </div>
</template>

<script>
import Parallax from 'parallax-js'
export default {
  name: 'UsessrPage',
  data() {
    return {
      //   calibrateX: false,
      //   calibrateY: true,
      //   invertX: false,
      //   invertY: true,
      //   limitX: false,
      //   limitY: 10,
      //   scalarX: 2,
      //   scalarY: 8,
      //   frictionX: 0.2,
      //   frictionY: 0.8,
      //   originX: 0.0,
      //   originY: 1.0,
    }
  },
  mounted() {
    this.init()
  },
  methods: {
    init() {
      const scene = document.getElementById('scene')
      const parallaxInstance = new Parallax(scene)
      this.parallaxObj = parallaxInstance
    },
  },
}
</script>

<style lang="scss" scoped>
#scene {
  position: relative;
  overflow: hidden;
  background: url(/yjzs/bg1.jpg) center/cover no-repeat;
  height: 100vh;
  margin: 0 auto;
}
</style>
