<template>
  <section class="section">
    <div class="columns is-mobile">
      <card
        title="Free"
        icon="github"
      >
        Open source on <a href="https://github.com/buefy/buefy">
          GitHub
        </a>
      </card>

      <card
        title="Responsive"
        icon="cellphone-link"
      >
        <b class="has-text-grey">
          Every
        </b> component is responsive
      </card>

      <card
        title="Modern"
        icon="alert-decagram"
      >
        Built with <a href="https://vuejs.org/">
          Vue.js
        </a> and <a href="http://bulma.io/">
          Bulma
        </a>
      </card>

      <card
        title="Lightweight"
        icon="arrange-bring-to-front"
      >
        No other internal dependency
      </card>
    </div>
    <form>
    <div class="mb-4">
      <label for="password1">Password</label>
      <VuePassword
        v-model="password1"
        id="password1"
        :strength="strength"
        type="text"
        disableStrength="false"
      />
    </div>
</form>
  </section>
</template>

<script>
import Card from '~/components/Card'
import VuePassword from 'vue-password'
// var $ = require('jquery');
// require('hideshowpassword');

// $('#password').togglePassword(); 

export default {
  el: '#app',
  components: {
    VuePassword,
    Card
  },
  data(){return{
    password1: "",
    strength: 0,
  }}
}
</script>
