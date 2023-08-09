<script setup>
// creating reactive data method 1 
import { ref, reactive } from "vue";

// ref method of data binding
const todo = ref("test");
console.log(todo.value);   // have to use .value to access the value within the script tag. Within template can just use todo

// reactive method of data binding
// const todoState = reactive({
//     todo: "This is a test",
// });
// To access the reactive method just do todoState.todo
</script>


<template>
    <div class="input-wrap">
        <input type="text" v-model="todo" />
        <button>Create</button>
    </div>
    <!-- <p>{{ todo }}</p> -->
</template>


<style lang="scss" scoped>
.input-wrap {
  display: flex;
  transition: 250ms ease;
  border: 2px solid #41b080;

  &:focus-within {
    box-shadow: 0 -4px 6px -1px rgb(0 0 0 / 0.1),
      0 -2px 4px -2px rgb(0 0 0 / 0.1);
  }

  input {
    width: 100%;
    padding: 8px 6px;
    border: none;

    &:focus {
      outline: none;
    }
  }

  button {
    padding: 8px 16px;
    border: none;
  }
}
</style>