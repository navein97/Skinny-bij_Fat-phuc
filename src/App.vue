<template>
  <img v-if="showImage1" src="./assets/fat_phuc.jpeg" alt="Image 1" />
  <img v-else src="./assets/skinny_bij.jpeg" alt="Image 2" />
  <h2>{{ name ? "Fat phuc" : "Skinny bij" }}</h2>
  <button @click="fatty">Click me bastard</button>
  <HelloWorld />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      name: true,
      showImage1: true,
    };
  },
  methods: {
    fatty() {
      this.name = !this.name;
      this.showImage1 = !this.showImage1;
    },
  },
};
</script>

<style>

button {
  background: linear-gradient(
    to right,
    #f4511e,
    #e91e63,
    #9c27b0,
    #673ab7,
    #3f51b5
  ); /* Slightly darker hues on hover */
    border: none;
    color: white;
    padding: 15px 32px; 
    text-align: center;
    font-size: 16px;
    cursor: pointer; 

    /* Optional Styling */
    border-radius: 5px;  /* Add rounded corners */ 
    box-shadow: 2px 3px 5px rgba(0, 0, 0, 0.2); /* Subtle shadow */
}

button:hover {
  background: linear-gradient(
    to right,
    #972708,
    #910a37,
    #650979,
    #3f1092,
    #162b95
  ); /* Slightly darker hues on hover */
}

img {
  max-width: 100%; /* Occupy maximum available width */
  max-height: 400px; /* Set a maximum height */
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
