<template>
  <p>Reaction time: <span class="score">{{ score }}</span> ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
  export default {
    props: ['score'],
    data() {
      return {
        rank: null
      }
    },
    mounted() {
      if (this.score < 200) {
        this.rank = "Ninja fingers"
      }
      else if (this.score < 325) {
        this.rank = "Rapid reflexes"
      }
      else {
        this.rank = "Snail pace..."
      }
    }
  }
</script>

<style>
  .score {
    font-style: bold;
  }

  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>