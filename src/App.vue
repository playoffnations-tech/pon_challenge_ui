<template>
  <div id="app" :class="'app--' + themeDefault" class="app">
    <Header :theme="themeDefault" :brand="brand"></Header>
    <PlayoffnationsChallenge :theme="themeDefault"></PlayoffnationsChallenge>
    <Footer :theme="themeDefault"></Footer>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import PlayoffnationsChallenge from "./components/PlayoffnationsChallenge.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default defineComponent({
  components: {
    PlayoffnationsChallenge,
    Header,
    Footer,
  },
  data() {
    return {
      themeDefault: "dark",
      brand: "Playoffnations"
    };
  },
});
</script>

<style>
*, ::after, ::before{
  box-sizing: border-box;
}

html,
body {
  margin: 0;
  padding: 0;
}

.app--dark {
  background-image: url("https://overworld.qodeinteractive.com/wp-content/uploads/2019/11/h3-page-bg-img.jpg");
  background-repeat: repeat;
  background-position: 0 0;
}

.app--light {
}
</style>
