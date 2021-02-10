<template>
  <div>
    <h1>Results</h1>
    <p>Reaction Time: {{ newScore }} ms</p>
    <p class="class">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ['newScore'],
  data () {
    return {
      rank: null
    }
  },
  mounted(){
    if(this.newScore < 250){
      this.rank = 'Ninja Fingers!'
    }
    else if(this.score < 400){
      this.rank = 'Rapid Fingers'
    }
    else{
      this.rank = 'What were you doing?'
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
