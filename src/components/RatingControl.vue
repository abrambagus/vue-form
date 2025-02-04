<template>
  <ul>
    <li :class="{ active: activeOptions === 'poor' }">
      <button @click="activate('poor')" type="button">Poor</button>
    </li>
    <li :class="{ active: activeOptions === 'averange' }">
      <button @click="activate('averange')" type="button">Averange</button>
    </li>
    <li :class="{ active: activeOptions === 'great' }">
      <button @click="activate('great')" type="button">Great</button>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      activeOptions: null,
    };
  },
  methods: {
    activate(option) {
      this.activeOptions = option;
    },
  },
};
</script>

<style scoped>
.active {
  border-color: purple;
}
.active button {
  color: purple;
}
ul {
  list-style: none;
  margin: 0.5rem 0;
  padding: 0;
  display: flex;
}

li {
  margin: 0 1rem;
  border: 1px solid #ccc;
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

button {
  font: inherit;
  border: none;
  background-color: transparent;
  cursor: pointer;
}
</style>
