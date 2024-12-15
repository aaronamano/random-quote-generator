<template>
  <div>
    <div class="quote-container">
      <div class="quote-content">
        <h1>Random Quote Generator</h1>
        <p>{{ quote.content }}</p>
        <p>- {{ quote.author }}</p>
        <button @click="generateQuote">Generate New Quote</button>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quotes: [
        { content: "Two cobras in the jungle. One kills the strongest lion, the other kills a crippled monkey. Which cobra do you want to be?", author: "Johnny Lawrence" },
        { content: "I may not always win, but I never back out of a fight.", author: "Johnny Lawrence" },
        { content: "Never mind your past mistakes; don’t let them determine your future.", author: "Carmen Diaz" },
        { content: "Put good into the world and good will come back to you..", author: "Kumiko" },
        { content: "Many of us used to be enemies. But rivalries don’t need to last forever.", author: "Daniel LaRusso" },
        { content: "We may have taken some losses. But it’s not about how you start, it’s about how you finish.", author: "Robby Keene" },
        { content: "If I’m extra hard on you, it’s because you have the ability to be better than me.", author: "Johnny Lawrence" },
        { content: "You’re a sensei. It’s who you are. If you can’t see that, you’re blind.", author: "Miguel Diaz" },
        { content: "Everybody’s got a sob story. Doesn’t give you the right to be a bully.", author: "Samantha LaRusso" },
        { content: "We’ve been here five minutes, and I’ve already seen ten people I hate. It’s Christmas alright.", author: "Amanda LaRusso" },
        { content: "There’s no honor in being merciless.", author: "Miguel Diaz" },
        { content: "A true cobra feels no sympathy for its meals.", author: "John Kreese" },
        { content: "If you have hate in your heart, then you have already lost.", author: "Daniel LaRusso" },
        { content: "When the fight comes to you, you have to be ready to fight back.", author: "Daniel LaRusso" },
        { content: "You just gotta feel the energy and just live in the moment, you know?", author: "Hawk" },

      ],
      quote: { content: "", author: "" }
    }
  },
  methods: {
    generateQuote() {
      const randomIndex = Math.floor(Math.random() * this.quotes.length);
      this.quote = this.quotes[ randomIndex ];
    }
  },
  mounted() {
    this.generateQuote();
  }
}
</script>

<style scoped>
.quote-container {
  max-width: 600px;
  margin: 0 auto;
  text-align: center;
  padding: 10px;
  font-size: 15px;
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 400px; /* Adjust this value as needed */
  max-width: 600px;
}

.quote-content {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;

  p {
    color: rgb(177, 14, 14);
    font-size: 18px;
  }

  h1 {
    color: rgb(7, 80, 5);
  }


}

button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  background-color: white;
  color: rgb(177, 14, 14);
  border-radius: 5px;
  border-color: #635518;

}

button:hover {
  background-color: rgb(7, 80, 5);
  color: yellow;
}
</style>

<style>
body {
  background-color: #f0cf31;
}
</style>
