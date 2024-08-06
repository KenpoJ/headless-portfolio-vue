<script setup></script>

<template>
  <header class="top-header">
    <div class="container">
      <div class="identity">
        <img class="logo" src="@/assets/img/arrow_logo_white.svg" alt="Jason Lyman mark" />
        <h1>Jason Lyman<br /><small>Web Designer & Developer</small></h1>
      </div>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/abstracts/_abstracts';

.top-header {
  padding: 10px 0;
  color: $light;
  text-align: center;
  background-color: $dark;

  .identity {
    display: flex;
    flex-direction: column;
    gap: 10px;
    align-items: center;
  }
  .logo {
    width: 100px;
    height: 100px;
  }

  @media (min-width: $md-breakpoint) {
    text-align: left;
    place-items: start;

    .identity {
      flex-direction: row;
      gap: 20px;
    }
  }
  h1 {
    font-size: 2rem;
    line-height: 1.2;
    color: $white;
  }

  nav {
    display: flex;
    gap: 20px;
    justify-content: center;

    @media (min-width: $md-breakpoint) {
      margin-top: 2rem;
      justify-content: flex-start;
    }

    a {
      color: $white;
      text-decoration: none;
      font-size: 1.2rem;
      transition: color 0.3s;

      &:hover {
        color: $medium-light;
      }
    }
  }
}
</style>
