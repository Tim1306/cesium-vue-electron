<template>
  <div id="cesiumContainer"></div>
</template>

<script>
import 'cesium/Build/Cesium/Widgets/widgets.css'
import * as Cesium from 'cesium'

Cesium.Ion.defaultAccessToken =
  'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiJhZmM3M2RiZS05YzVjLTRkNzktYTgyNS1mZjQ0ODYxNzhhMDgiLCJpZCI6MTAzMjkyLCJpYXQiOjE2NTk0MTAxNjJ9.EXOKIrOawerE9ATAyHBFuoYf2MW3XXxzlt78D5V8g5k'
export default {
  name: 'CesiumContainer',
  mounted() {
    /* eslint no-new: */
    this.initCesium()
  },
  methods: {
    initCesium(){
      let viewer = new Cesium.Viewer('cesiumContainer')
      window.viewer = viewer
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#cesiumContainer {
  width: 100%;
  height: 100%;
}
</style>
