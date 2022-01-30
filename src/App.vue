<template>
  <div class="container">
    <Header
      @toggle-add-task="toggleAddTask"
      title="Task Tracker"
      :showAddTask="showAddTask"
    />
    <router-view :showAddTask="showAddTask"></router-view>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header";
import Footer from "./components/Footer";
export default {
  name: "App",
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      showAddTask: false,
    };
  },
  methods: {
    toggleAddTask() {
      this.showAddTask = !this.showAddTask;
    },
  },
};

console.log(
  "%c Hi, wanna see some console? \n" +
    "%c Well, feel free to check it out and play with it! \n" +
    "%c But don't hack my website tho... \n" +
    "%c Or... get hacked! \n" +
    "%c Also, have a nice day!",
  "color: #5865f2; font-size: 1.5em; font-weight: bold; line-height: 1.22; letter-spacing: 1em;",
  "color: #8C97EA; font-size: 1.5em; font-weight: bold; line-height: 1.22; letter-spacing: 1em;",
  "color: #DA3940; font-size: 1.5em; font-weight: bold; line-height: 1.22; letter-spacing: 1em;",
  "color: #D90000; font-size: 1.5em; font-weight: bold; line-height: 1.22; letter-spacing: 1em;",
  "color: green; font-size: 1.5em; font-weight: bold; line-height: 1.22; letter-spacing: 1em;"
);
console.warn(
  "Anyways check out this linky link: \n https://bit.ly/3xiWaWh <- Clicky click the linky link"
);
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: "Poppins", sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
