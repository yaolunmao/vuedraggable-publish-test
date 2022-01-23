<template>
  <draggable
    v-model="myArray"
    group="people"
    @start="drag = true"
    @end="drag = false"
    item-key="id"
  >
    <template #item="{ element }">
      <div>{{ element.name }}</div>
    </template>
  </draggable>
  <!-- If you annotate the above, the following components will be published successfully -->
  <!-- <button>test publish btn</button> -->
</template>

<script setup lang="ts">
import { reactive, ref } from 'vue';
import draggable from 'vuedraggable';
const myArray = ref([
  { name: "John", id: 1 },
  { name: "Joao", id: 2 },
  { name: "Jean", id: 3 },
  { name: "Gerard", id: 4 }
]);
const drag = ref(false);
</script>

<style>

</style>