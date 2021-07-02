<template>
  <p>Initial Value: {{initialValue}}</p>
  <p>Actual Value: {{count}}</p>
  <button @click="add">Add</button>
</template>

<script>
import {ref} from "vue";

export default {
  name: 'Counter',
  props: {
    initialValue: Number
  },
  setup(props){
    console.log(props);

    const count= ref(props.initialValue);

    const add = () => {
      count.value++;
    }

    return {count, add}
  }
}
</script>

<style scoped>

</style>
