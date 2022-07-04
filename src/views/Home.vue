<template>
  <div id="home">
    <table class="attributes" v-if="isShow">
      <tr>
        <th>水平对正</th>
        <td>中心</td>
      </tr>
      <tr>
        <th>参照标高</th>
        <td>50.0 mm</td>
      </tr>
      <tr>
        <th>坡度</th>
        <td>0.0000%</td>
      </tr>
      <tr>
        <th>尺寸</th>
        <td>1800*1100*1500 mm</td>
      </tr>
      <tr>
        <th>材质</th>
        <td>钢、碳钢</td>
      </tr>
      <tr>
        <th>系统分类</th>
        <td>循环供水</td>
      </tr>
      <tr>
        <th>系统类型</th>
        <td>F冷却水供水驱动</td>
      </tr>
      <tr>
        <th>连接类型</th>
        <td>常规</td>
      </tr>
      <tr>
        <th>粗糙度</th>
        <td>0.04600mm</td>
      </tr>
      <tr>
        <th>规格/类型</th>
        <td>Schedule 40</td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
      <tr>
        <th></th>
        <td></td>
      </tr>
    </table>
  </div>
</template>

<script>
import Viewer from "@/core/viewer.js";

export default {
  name: "Home",
  data() {
    return {
      viewer: null,
      viewerEl: null,
      isShow: false
    }
  },
  mounted() {
    this.viewerEl = document.getElementById("home");
    this.viewer = new Viewer(this.viewerEl);
    this.viewer.load('files/gltf/NewProject.gltf');
  }
};
</script>

<style scoped>
#home {
  width: 100vw;
  height: 100vh;
}
.attributes {
  display: block;
  height: 300px;
  position: absolute;
  right: 10px;
  top: 10px;
  border: 3px solid #aaa;
  border-collapse: collapse;
  overflow-y: scroll;
}
.attributes td {
  height: 30px;
  text-align: center;
  border: 1px solid #aaa;
}
.attributes th {
  height: 30px;
   text-align: center;
   border: 1px solid #aaa;
 }

</style>
