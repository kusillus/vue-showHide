<template>
  <div id="app">
    <div class="container">
      <!-- Header -->
      <div class="header">
        <h5 class="ml-2 title-filter">Filtros</h5>
        <span class="mr-2 dropUpBtn" @click="show = !show">
          <i v-if="show"><svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M7,10L12,15L17,10H7Z" /></svg></i>
          <i v-else><svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22M17,14L12,9L7,14H17Z" /></svg></i>
        </span>
      </div>
      <!-- body -->
      <transition name="changeHeight">
        <div v-if="show">
          <p>Servine Serperior Tepig Pignite Emboar Oshawott Dewott Samurott Patrat Watchog Lillipup Herdier Stoutland Purrloin Liepard Pansage Simisage Pansear Simisear Panpour Simipour Munna Musharna Pidove Tranquill Unfezant Blitzle Zebstrika Roggenrola Boldore Gigalith Woobat </p>
        </div>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      show: true,
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100%;
  display: flex;
  justify-content: center;
}
.container {
  width: 90%;
  display: flex;
  flex-flow: wrap;
  justify-content: center;
  box-shadow: 0rem 0rem 1rem 0px rgba(0, 0, 0, 0.60);
  transition: all 1s;
}
.header {
  background-color: #26C6DA;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}
.changeHeight-leave-active {
  transition: all .3s;
  max-height: 500px;
}

.changeHeight-enter-active {
  transition: all .7s;
  max-height: 300px;
}
.changeHeight-enter,
.changeHeight-leave-to
{
  opacity: 0;
  max-height: 0px;
}
</style>
