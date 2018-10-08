<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <div v-if="connected">
      <HelloWorld msg="Hola ;)"/>
    </div>
    <div v-else>
      <span>connecting...</span>    
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  computed: {
    connected(){
      return this.$store.state.sdp.isConnected
    }
  }
}
</script>
