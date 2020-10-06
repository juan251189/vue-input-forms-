<template>
<div>
  <div id="on" @click="isSwitched(true)" :class="{active: switched}">
    On
  </div>
  <div id="off" @click="isSwitched(false)" :class="{active: !switched}">
    Off

  </div>
</div>
</template>
<script>
export default {
props: ['switched'],
  methods: {
    isSwitched(value) {
      this.$emit('input',value);

    }
  }
}
</script>
<style>
#on,
#off {
  width: 40px;
  height: 20px;
  background-color: lightgray;
  padding: 2px;
  display:inline-block;
  margin:10px -2px;
  box-sizing: content-box;
  cursor:pointer;
  text-align: center;


}

#on:hover, #on.active{
  background-color:lightgreen;

}

#off:hover, #off.active{
  background-color: lightcoral;

}
</style>
