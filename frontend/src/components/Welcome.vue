<template>
	<b-card 
    class="align-center"
    header-tag="header">
    <b-form id="welcomeForm" @submit.prevent="">
      <b-form-group vertical
                    label="Username"
                    label-for="Username"
                    class="form-vertical-align">
      <b-form-input id="Username"
                      v-model="credentials.username"
                      required
                      placeholder="Username" disabled>
     </b-form-input>
     </b-form-group>
     <b-form-group vertical
                    label="Password"
                    label-for="Password"
                    class="form-vertical-align">
     <b-form-input id="Password" type="password"
                      v-model="credentials.password"
                      required
                      placeholder="Password" disabled>
     </b-form-input>
     </b-form-group>
   </b-form>
  </b-card>
</template>

<script>
export default {
  mounted() {
    console.log("hellooooo ready!!");
    this.credentials.username = localStorage.getItem("userName")
    this.credentials.password = localStorage.getItem("userPassword")
  },
  data() {
    return {
      credentials: {
        username: "",
        password: ""
      }
    };
  },
  methods: {
  }
};
</script>