<template>
  <div class="home">
   <!-- Page Header -->
    <header class="masthead" style=''>
      <div class="overlay"></div>
      <div class="container">
        <div class="row">
          <div class="col-lg-8 col-md-10 mx-auto">
            <div class="site-heading">
              <h1>Welcome Go-Bloggers</h1>
              <span class="subheading">A Blog Web by Agung Atidhira</span>
            </div>
          </div>
        </div>
      </div>
    </header>
     <!-- 
      <h6 v-if='isLogin'>Bitcoin Price Index</h6>
      {{info.data.bpi.USD.code}} : {{info.data.bpi.USD.rate}}
      -->

    <div class="row">
      <div class="side-bar col-md-3">
        <SideBar :isLogin='isLogin' :getDate='getDate' ></SideBar>
      </div>
      <div class="main-content col-md-9">
        <MainContaint  :isLogin='isLogin' :getDate='getDate'></MainContaint>
      </div>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import MainContaint from "@/components/mainContaint.vue";
import SideBar from "@/components/sideBar.vue";

export default {
  props: ['isLogin', 'getDate'],
  name: 'home',
  data () {
    return {
      info: null
    }
  },
  mounted () {
    
  },
  components: { 
    MainContaint, SideBar
  },
  methods: {
    
  },
  watch: {
   
  }
}
</script>

<style>
.masthead {
  background-image: url('../assets/home-bg.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: 50% 20%; 
  background-size: cover;
}

.site-heading {
  color: whitesmoke;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}

</style>
