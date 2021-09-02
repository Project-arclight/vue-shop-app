<template>
  <div class="home">
    <router-link :to="{name:'Items',params:{id:1}}">
      item 1
    </router-link>
       <router-link :to="{name:'Items',params:{id:2}}">
      item 2  
    </router-link>
       <router-link :to="{name:'Items',params:{id:3}}">
      item 3
    </router-link>
    {{data}}
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios'
export default {
  name: 'Home',
  data(){
    return{
      characters:null
    }
  },mounted(){
    const response =axios.get("https://api.genshin.dev/characters/")
    console.log(response)
  },
  methods:{
    getCharacters(){
      

    }
  }
}
</script>
