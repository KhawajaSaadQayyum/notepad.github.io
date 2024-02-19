<template>
  <div class="overlay">
    <textarea name="textarea" id="aread" cols="50" rows="10"></textarea>
    <button @click="addNotes">Add Notes</button>
    <button>Close</button>
  </div>
  <div class="main-container">
    <div class="heading"><h1>Add Notes</h1></div>
    <div class="add-Button">+</div>
  </div>

  <div class="cards-container">
    <div class="cards">
      <p class="notes">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi laborum
        consectetur quia dicta atque consequatur autem iste ex enim
        reprehenderit fuga aliquid, voluptate quaerat asperiores!
      </p>

      <p class="dete">20/10/2023</p>
    </div>
  </div>

  <!-- <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
  </div> -->
</template>
<script setup lang="ts">
import { ref } from "vue";

// defineProps<{ msg: string }>();
let showOverlay = ref(false );
addNotes(){

  showOverlay == true;
}
</script>
<style scoped>
.main-container {
  max-height: 1000vw;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.add-Button {
  background-color: black;
  /* margin: 10px; */
  padding: 20px;
  color: white;
  font-size: 30px;
  font-weight: bold;
  border-radius: 50%;
  cursor: pointer;
}
.cards-container {
  display: flex;
  flex-wrap: wrap;
  margin: 30px;
}
.cards {
  width: 300px;
  margin: 10px;
  height: 300px;
  background-color: aquamarine;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 15px;
}
.notes {
  margin: 10px;
  color: black;
}
.dete {
  margin: 10px;
  position: relative;
  color: black;
  margin-bottom: 10px;
  font-size: bold;
  font-size: 18px;
}
.overlay {
  width: 100%;
  height: 100%;
  z-index: 100;
  position: absolute;
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
  background-color: rgba(0, 0, 0, 0.216);
}
</style>
