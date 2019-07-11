<template>
  <div class="hello">
    <span v-if="seen">Now you see me</span>
    <input type="radio" id="yes" value="yes" v-model="test"> yes
    <br>
    <input type="radio" id="no" value="no" v-model="test"> no
    <p v-if="test === 'yes'" >👍</p>
    <p v-else-if="test === 'no'" >True</p>
    <br>
    <label>Input Score : </label>
    <input type="input" value="" v-model="score">
    <br>
    <p v-if="score >= '80' && score <= '100'" >A</p>
    <p v-else-if="score >= '75' && score <= '79'" >B+</p>
    <p v-else-if="score >= '70' && score <= '74'" >B</p>
    <p v-else-if="score >= '65' && score <= '69'" >C+</p>
    <p v-else-if="score >= '60' && score <= '64'" >C</p>
    <p v-else-if="score >= '55' && score <= '59'" >D+</p>
    <p v-else-if="score >= '50' && score <= '54'" >D</p>
    <p v-else-if="score >= '0' && score <= '49'" >F</p>

    <input type="checkbox" id="Banana" value="Banana" v-model="Fruit">
    <label for="john"> Banana</label>
  
    <input type="checkbox" id="Apple" value="Apple" v-model="Fruit">
    <label for="paul"> Apple</label>
  
    <input type="checkbox" id="Mango" value="Mango" v-model="Fruit">
    <label for="george"> Mango</label>
  
  <br>
  <span>Fruit to me: {{ Fruit }}</span>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
    seen: false,
    test:'',
    score:'',
    Fruit:[]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
