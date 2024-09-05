

<script setup>
  import { ref }  from 'vue'
  let id = 0
  const ListeTache = ref([
    {id: id++,nom:'Apprendre PHP'},
    {id: id++,nom:'Apprendre Vue'},
    {id: id++,nom:'Apprendre JAVA'}
  ])
</script>

<template>
  <h1>To Do List</h1>
  <input type="text"/>
  <button>Ajouter</button>
  <br/>
  <h3>Liste des Tâches</h3>
  <ul>
    <li v-for="tache in ListeTache " :key="tache.id">
      {{tache.id}} {{tache.nom}}
    </li>
  </ul>
</template>

<style scoped>

</style>
