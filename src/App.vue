<template>
  <div id="app">
  
    <Entrance id="Entrance"/>
    <Web :field="sharedState.seedData[1]"   id="Web"/>
    <Robotics :field="sharedState.seedData[2]" id="Robotics"/>
    <Android :field="sharedState.seedData[3]" id="Android"/>
    <ML :field="sharedState.seedData[4]" id="ml"/>

  </div>
</template>

<script>

import Entrance from './components/Entrance.vue'
import Android from './components/Android.vue'
import ML from './components/ML.vue'
import Web from './components/Web.vue'
import Robotics from './components/Robotics.vue'
import { store } from './store.js';

export default {
  name: 'app',
  data () {
    return {
      sharedState: store.state
    }
  },
  props: ['this.sharedState'],
  components:{
    Entrance,
    Web,
    ML,
    Android,
    Robotics
  },
  methods: {
  }
}
</script>

<style>

</style>
