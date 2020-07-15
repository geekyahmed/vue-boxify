<template>
  <div class="container">
    <div class="box" :style="boxStyle"></div>
    <div>
     <br/><label>Background Color: </label> <input type="text" class="form-control" v-model="backgroundColor">
      <br/><label>Width: </label> <input type="text" class="form-control" v-model="width">
      <br/><label>Height: </label> <input type="text" class="form-control" v-model="height">
    </div>
  </div>
</template>

<script>
export default {
  name: "Box",
  data() {
    return {
      backgroundColor: "gray",
      width: 200 ,
      height: 200
    };
  },
  computed: {
    boxStyle: function() {
      return {
        backgroundColor: this.backgroundColor,
        width: this.width + 'px',
        height: this.height + 'px'
      };
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
font-family: Poppins;
}
.box {
  width: 200px;
  height: 200px;
  background-color: gray;
  display: inline-block;
  border-radius: 20px;
}
.form-control{
  text-align: center;
  border: none;
  outline: none;
  background-color: #e5e5e5;
  border-radius: 20px;
  height: 50px;
  padding: 10px 10px 10px;
  margin-top: 20px;
  }
</style>
