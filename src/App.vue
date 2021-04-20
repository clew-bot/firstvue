<template>
<div class="container">
 <Header title="Task Tracker"/>
 <Tasks :tasks="tasks"/>
</div>

</template>

<script>

import Header from "./components/Header"
import Tasks from "./components/Tasks"
export default {
  name: 'App',
  // components
  components: {
    Header,
    Tasks,
  },
  data() {
    return {
      tasks: [],
    }
},
created() {
  this.tasks = [{
    id: 1,
    text: "Go to Interview",
    day: "April 20th at 2:00",
    reminder: true,
  },
  {
    id: 2,
    text: "Go to Dog Show",
    day: "April 23th at 4:00",
    reminder: true,
  },
  {
    id: 3,
    text: "Go to Work",
    day: "April 27th at 9:00",
    reminder: false,
  },
  {
    id: 4,
    text: "Go to Disneyland",
    day: "April 22th at 7:00",
    reminder: true,
  },
  ]}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
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
