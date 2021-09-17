<template>
    <div class="test">
      <input type="text" v-model="text" @keypress.enter="add">
      <p v-for="task   in todo_list" v-bind:key="task">
        {{task}}
      </p>
    </div>
</template>

<script>
export default {
    name:"Test",

    data(){
      return{
        todo_list:[],
        text:""
      }
    },
    methods:{
      add(){
        this.todo_list.push(this.text)
        this.text = ""
      }
    }
}
</script>

<style>

</style>