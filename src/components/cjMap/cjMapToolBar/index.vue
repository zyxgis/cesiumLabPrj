<!-- 工具条 -->
<template>
  <div class="map-tool-bar">
    <cj-tool></cj-tool>
    <base-map v-show="!is3dMap"></base-map>
    <base3DMap v-show="is3dMap"></base3DMap>
  </div>
</template>

<script>
import baseMap from "./baseMap";
import base3DMap from "./base3dMap";
import cjTool from "./cjTool";

export default {
  data() {
    return {};
  },

  components: { baseMap, base3DMap, cjTool },

  computed: {
    is3dMap() {
      return this.$store.state.map.is3dMap;
    }
  },

  mounted() {},

  methods: {},
  destroyed: {}
};
</script>
<style lang='scss' scoped>
.map-tool-bar {
  position: absolute;
  top: 40px;
  right: 110px;
  background: #ffff;
  padding: 8px;
  border-radius: 5px;
}
</style>