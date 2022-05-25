<template>
    <p>Reaction Time : {{ score }}</p>
    <p class="rank">Rank : {{ rank }}</p>
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
            this.rank = 'Ninja Fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid Reflexes'
        } else {
            this.rank = 'Snail Pace...'
        }
    }
}
</script>

<style>

</style>