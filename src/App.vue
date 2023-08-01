<template>
  <div class="container">
    <h1 v-color>test1</h1>
    <!-- <h1 v-colorred="colorred">TEST2</h1> -->
    <h2 v-color="'green'">test3</h2>
    <button @click="color='blue'">change color</button>
    <hr>

    <div>
      <Left></Left>
    </div>
  </div>
</template>

<script>
import Left from '@/components/Left.vue'

export default {
  data() {
    return {
      color:'red'
    }
  },
  directives: {
    color: {
      bind(el,binding) {
        console.log('touch off')
        console.log(el,binding)
        el.style.color = binding.value
      },
      update(el,binding) {
        el.style.color=binding.value
      }
    }
  },
  methods: {
    // change() {
    //   this.style.color='biue'
    //   console.log(this)
    // }
  },
  components: {
    Left
  }
 }
</script>

<style >
  /* .container{
    
   
  } */
</style>

1123124
