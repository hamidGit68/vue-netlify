<template>
  <div id="app">
    <preloader></preloader>
    <!-- the "header1" component is used for header part of the web and is repeated in every page  -->

    <section id="mainContents" v-if="showCont">
      <header1></header1>
      <theNanigation></theNanigation>
      <router-view />
      <footerBook></footerBook>
    </section>
  </div>
</template>

<script>
import header1 from "./components/header1.vue";
import theNanigation from "./components/theNanigation";
import Preloader from "./components/preloader";
import footerBook from "./components/footerBook";
export default {
  data() {
    return {
      showCont: false
    }
  },
  components: {
    Preloader,
    header1,
    theNanigation,
    footerBook
  }

};
</script>

<style src="../public/styles/style.css"></style>
