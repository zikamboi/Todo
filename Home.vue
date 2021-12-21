<template>
<h1> TO do App<h1/>
<form @submit.prevent = "addNewTodo">
<label> New Todo</label>
<input v-model = "newTodo" name="newTodo">
<button> Add New Todo </button>
</form>
</template>

<script>

import { ref} from 'vue';

export default {
    setup() {
        const newTodo = ref ('');

        function addNewTodo() {
            console.log(newTodo.value);
        } 
            return { 
                newTodo,
                addNewTodo, 
        };
    }
}
</script>

<style>

body
{
    font-family : sans-serif;
    padding-top: 1em;
    padding-bottom: 1em;
    font-size: 2em;
    width:80%;
    margin: 0 auto; 
}
