<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">BAYES.ID</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#" @click.prevent="toHome"
            >Home <span class="sr-only">(current)</span></a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" @click.prevent="$router.push('/addProduct')">Add Products</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#" @click.prevent="logout">Logout</a>
        </li>

      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavbarHome',
  methods: {
    logout () {
      localStorage.removeItem('access_token')
      this.$router.push('/login')
    },
    toHome () {
      this.$router.push('/')
    }
  }
}
</script>

<style></style>
