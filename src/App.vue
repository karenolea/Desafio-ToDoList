<template>
  <div id="app">
     <h1>Crea una nueva tarea</h1>
        <label for="">Tarea</label>
        <input v-model="respuesta" placeholder="ingresa nueva tarea">
        <button @click="btn">Crear</button> 
    <h4>Lista</h4>
        <ul v-for="(dato, index) in tareas" :key="index">
            <li>
              <p> {{index}} {{dato}}</p>
            </li>
        </ul>
  </div>
</template>


<script>
export default {
    name:"App",
    data(){
         return{
            respuesta:"",
            tareas:[],

        }  
    },
    methods: {
        btn (){
            this.tareas.push(this.respuesta)
            this.respuesta=""
        }
        
        
    }
};
</script>
<style scoped>
#app {
    padding: 3rem;
}
label{
    font-size: 1.3rem;
}
h4{
    padding: 1rem;
    margin-left: 3rem;
}
</style>
