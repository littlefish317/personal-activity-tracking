<template>
  <div>
    <h1>Hello World</h1>
    <h2>I am {{ name }}</h2>
    <input v-model="age" />
    <ul v-if="quests">
      <li v-for="quest in quests" :key="quest.id">
        {{ quest.id }} {{ quest.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Katie",
      age: 15,
      quests: [
        {
          id: 1,
          name: "first"
        },
        {
          id: 2,
          name: "second"
        }
      ]
    };
  },
  computed: {
    shouldId: function() {
      if (this.age < 21) {
        return true;
      } else {
        return false;
      }
    }
  }
};
</script>

<style scoped></style>
