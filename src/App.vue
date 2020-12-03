<template>
  <div id="app">
    <Kanban :data="data" :create_task_submit="create_task_submit"/>
  </div>
</template>

<script>
import Kanban from "./components/Kanban"
export default {
  name: 'App',
  components: {
    Kanban
  },
  data(){
    return {
      data:[
        {
          name:"todo",
          color:"#F5B271",
          tasks:[
            {
              task_name:"tesk"
            }
          ]
        },
         {
          name:"doing",
          color:"#BEA771",
          tasks:[
                       {
              task_name:"tesk"
            }
          ]
        },
         {
          name:"done",
          color:"#1B796F",
          tasks:[
                       {
              task_name:"tesk"
            }
          ]
        }
      ]
    }
  },
  methods:{
    create_task_submit(colum_index,item){
      this.data[colum_index].tasks.push(item)
    }
  }
}
</script>

<style>
  #app {
  height: 100vh;
  }
</style>
