<template>
  <nav class="navbar navbar-expand-lg navbar-light">
  <a class="navbar-brand" href="#">Kanban</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item">
        <a class="nav-link" id="btn-login" href="#" @click.prevent="loginForm">Login</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" id="btn-register" href="#" @click.prevent="registerForm">Register</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" id="btn-logout" href="#" @click.prevent="logout">Logout</a>
      </li>
      </ul>
  </div>
</nav>
</template>

<script>
export default {
    name: 'Navbar',
    props: ['isPage'],
    methods: {
        loginForm(){
            this.$emit('changePage', 'login')
        },
        registerForm(){
            this.$emit('changePage', 'register')
        },
        logout(){
            localStorage.clear()
            this.$emit('changePage', 'login')
        }
    }
}
</script>

<style>

</style>