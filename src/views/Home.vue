<template>
  <div class="monster-grid">
    <navbar-component > </navbar-component >

    <main class="main">
      <header-layout></header-layout>
      <skills></skills>
      <portafolio-vue></portafolio-vue>
    </main>
    <footer-layout ></footer-layout >
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarComponent from "../components/NavbarComponent.vue";
import FooterLayout from "../components/FooterLayout.vue";
import HeaderLayout from "../components/HeaderLayout.vue";
import PortafolioVue from '../components/Portafolio.vue';
import Skills from '../components/Skills.vue';
export default {
  name: "home",
  components: {
    NavbarComponent,
    FooterLayout,
    HeaderLayout,
    PortafolioVue,
    Skills
  },
 
  methods: {
    goTodetail(proId, name, description) {
      let query = {
        proId: proId,
        name: name,
        description: description
      };
      return this.$router.push({ name: "details", params: query }); // -> /user/123
    }
  }
};
</script>
