<template>
  <div class="container">
    <h1>🔮 Fortune Teller 🔮</h1>
    <p>{{ fortune }}</p>
    <button @click="getFortune">Get Your Fortune</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const fortunes = [
      "You will have a great day! 🌟",
      "A surprise is waiting for you! 🎁",
      "An opportunity will come your way! 🚀",
      "Expect good news soon! 📩",
      "Someone is thinking of you! 💌",
      "Your hard work will pay off! 💰",
      "Your kindness will be rewarded! 🏆"
    ];

    const fortune = ref("Click the button to reveal your fortune!");

    const getFortune = () => {
      const randomIndex = Math.floor(Math.random() * fortunes.length);
      fortune.value = fortunes[randomIndex];
    };

    return { fortune, getFortune };
  }
};
</script>

<style scoped>

</style>
