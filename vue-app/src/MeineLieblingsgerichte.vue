<template>
  <div>
    <h1>Meine Lieblingsgerichte 🍝</h1>

    <!-- Nur anzeigen, wenn es überhaupt Gerichte gibt -->
    <ul v-if="gerichte.length > 0">
      <li v-for="(gericht, index) in gerichte" :key="index">
        {{ index + 1 }}. {{ gericht }}
      </li>
    </ul>

    <!-- Wenn Liste leer ist -->
    <p v-else>Keine Gerichte gefunden 😢</p>
  </div>
</template>

<script setup>
const gerichte = ["Pizza", "Sushi", "Tacos", "Pasta"]
// Probiere auch mal: const gerichte = []
</script>

<style scoped>
h1 {
  color: #42b983;
  font-family: sans-serif;
}
p {
  color: gray;
  font-style: italic;
}
</style>

