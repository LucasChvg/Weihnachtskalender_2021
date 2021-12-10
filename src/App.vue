<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  components: {
    // imported Components go here
  },

  data() {
    return {
      count:0,
    };
  },

  methods: {
    increment(){
      this.count++;
    },
    reset(){
      this.count = 0;
    },
  },
});
</script>

<template>
  <h1>Weihnachtskalender 2021</h1>
  <div class="calendar">
    {{count}}
  </div>
  <button @click="increment">Click Me</button>
  <button @click="reset">Reset</button>
  <NumberDiv :Numbers="[0, 1, 2, 3]"/>
  <NumberDiv :Numbers="[4, 5, 6, 7]"/>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Mountains+of+Christmas:wght@700&display=swap");

#app {
  font-family: "Mountains of Christmas", cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 10px;
}

/* This creates a 6x4 grid with 140px wide squares */
.calendar {
  display: grid;
  grid-template-columns: repeat(6, 140px);
  grid-template-rows: repeat(4, 140px);
  gap: 20px;
}
</style>
