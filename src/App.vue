<template>
  <div id="app">
    <header>
      <button @click="page = 'page1'">page 1</button>
      <button @click="page = 'page2'">page 2</button>
    </header>

    <main>
      <page1 v-if="page == 'page1'"/>
      <page2 v-if="page == 'page2'"/>
    </main>
  </div>
</template>

<script>
import page1 from './components/page1.vue'
import page2 from './components/page2.vue'

export default {
  data: function(){
    return {
      page : "page1"
    }
  },
  name: 'App',
  components: {
    page1,
    page2
  }
}
</script>

<style>

</style>
