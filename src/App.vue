<template>
  <div id="app">
    <p>BluePrint Status: {{planStatus}}</p>
    <button @click="changePlanStatus">Change plan status</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      planStatus: 'In Progress',
      sponsor: 'Yet to be finalised'
    };
  },
  beforeCreate() {
    // alert("Status of conference plan: "+this.planStatus);
  },
  created() {
    // alert("In created hook, initial status of conference plan is : " + this.planStatus);
    this.planStatus = 'Blueprint finalised';
    // alert("In created hook, updated status of conference plan is: " + this.planStatus);
  },
  beforeMount() {
    // Print value of dom element 
    // console.log("Values of this.$el in beforeMount", this.$el);
  },
  mounted() {
    // Print value of dom element 
    // console.log("Values of this.$el in mounted", this.$el);
  },
  beforeUpdate() {
    // console.log("Value of plan status in beforeUpdate(): " + this.planStatus);
  },
  updated() {
    console.log("Value of plan status in updated():" + this.planStatus);
  },
  beforeDestroy() {
    this.planStatus = null;
    delete this.planStatus;
  },
  methods: {
    changePlanStatus() {
      // do smth
      this.planStatus = 'Event speaker changed';
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
