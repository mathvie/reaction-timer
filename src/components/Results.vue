<template>
  <p>Reaction time - {{ score }} ms </p>
  <p class="rank">{{ rank }} </p>
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
        if (this.score < 250) {
            this.rank = "You are a Ninja"
        } else if (this.score < 400) {
            this.rank = "Fast but you must to improve"
        } else {
            this.rank = 'Turtle steps'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>