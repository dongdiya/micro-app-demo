<!--
 * @Desc: 
 * @Author: dongdiya
 * @Date: 2022-11-15 14:04:20
 * @LastEditors: dongdiya
 * @LastEditTime: 2022-12-02 17:54:14
-->
<template>
  <div>
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>子应用 -- Vue@{{version}}</h1>
    <draggable v-model="myArray" group="people" @start="drag=true" @end="drag=false">
      <div v-for="element in myArray" :key="element.id">{{element.name}}</div>
    </draggable>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from '../components/HelloWorld.vue'
import Vue from 'vue'
import draggable from 'vuedraggable'
export default {
  name: 'page1',
  data () {
    return {
      version: Vue.version,
      myArray: [{id:1, name: 'aaa'},{id:2, name: 'bbb'},{id:3, name: 'ccc'},{id:4, name: 'ddd'},{id:5, name: 'eee'}]
    }
  },
  components: {
    HelloWorld,draggable
  },
}
</script>

<style>

</style>
