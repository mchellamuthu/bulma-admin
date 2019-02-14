<template>
  <div id="app" class="wrapper">
    <div class="sidebar" :style="menuActive ? 'display:block':'display:none'">
      <nav class="side-nav">
        <a href class="active">
         <span class="icon"> <i class="fa fa-home"></i> </span> 
         <span>Dashboard</span>
        </a>
        <a href class="">
         <span class="icon"> <i class="fa fa-home"></i> </span> 
         <span>Dashboard</span>
        </a>
        <a href class="">
         <span class="icon"> <i class="fa fa-home"></i> </span> 
         <span>Dashboard</span>
        </a>
        <a href class="">
         <span class="icon"> <i class="fa fa-home"></i> </span> 
         <span>Dashboard</span>
        </a>
        
      </nav>

    </div>
    <!-- <div class="site-overlay" :style="menuActive ? 'display:block':'display:none'" @click="toggleMenu"></div> -->
    <div class="bottom-bar is-hidden-mobile	">
      <div class="user-info">
        <div class="dropdown is-up is-hoverable">
          <div class="dropdown-trigger">
            <a href="javascript:void(0);" aria-haspopup="true" aria-controls="dropdown-menu">
              <img src="http://i.pravatar.cc/150?img=3">
              <span style="">Chellamuthu M</span>
              <span class="icon is-small">
                <i class="fas fa-angle-up" aria-hidden="true"></i>
              </span>
            </a>
          </div>
          <div class="dropdown-menu" id="dropdown-menu" role="menu">
            <div class="dropdown-content">
              <div class="dropdown-item">
                <p>You can add the
                  <code>is-up</code> modifier to have a dropdown menu that appears above the dropdown button.
                </p>
              </div>
            </div>
          </div>
        </div>
        <!-- <button class="button is-info shadow-sm">NEW PROJECT</button> -->
      </div>
      <div class="footer-custom"></div>
    </div>
    <div class="content">
      <div class="top-bar">
       <button class="button" @click="toggleMenu"> <span class="icon"><i class="fa fa-bars fa-2x"></i></span>  </button> 
      </div>
      <router-view/>
    </div>
  </div>
</template>
<script>
export default {
  name : "App",
  data() {
    return {
      menuActive  :false
    }
  },
  methods: {
    toggleMenu(){
     this.menuActive =  this.menuActive ? false : true;
    }
  },
}
</script>
<style lang="scss">
@import "./assets/scss/app.scss";
</style>
