<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo1.jpg" width="300" height="300" />

    <div class="wrapper">
      <HelloWorld msg="Hi Everyone!!" />
    </div>
  </header>
  <main>
    <TheWelcome/>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  border-radius: 100%;
  animation: moveUpDown 1.5s linear infinite alternate;
}

@keyframes moveUpDown {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-20px);
  }
}

.wrapper {
  animation: moveUpDownMsg 1.5s linear infinite alternate;
}

@keyframes moveUpDownMsg {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-20px);
  }
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>