<template>
  <div id="app">
    <div>
      <b-tabs content-class="mt-3">
        <b-tab title="Home" @click="component = 'Home'" active></b-tab>
        <b-tab title="Contact" @click="component = 'Contact'"></b-tab>
        <b-tab title="About" @click="component = 'About'"></b-tab>
      </b-tabs>
      <!-- <div>
        <button @click="component = 'Home'">Home</button>
        <button @click="component = 'Contact'">Contact</button>
        <button @click="component = 'About'">About</button>
      </div> -->
    </div>

    <component :is="component"></component>
  </div>
</template>

<script>
import Home from "./components/Home";
import Contact from "./components/Contact";
import About from "./components/About";

export default {
  name: "App",
  components: {
    Home,
    Contact,
    About,
  },
  data() {
    return {
      component: "Home",
    };
  },
};
</script>

<style>
</style>
