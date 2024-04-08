<script setup>
import MediumAside from '../components/templates/medium/MediumAside.vue';
import MediumFooter from '../components/templates/medium/MediumFooter.vue';
import MediumHeader from '../components/templates/medium/MediumHeader.vue';
</script>

<template>
    <div id="layout-medium">
        <header>
            <medium-header />
        </header>
        <aside>
            <medium-aside />
        </aside>
        <main>
            <router-view />
        </main>
        <footer>
            <medium-footer />
        </footer>
    </div>
</template>

<style scoped>
#layout-medium {
  display: grid;
  grid-template-columns: 1fr 5fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    'aside header'
    'aside main'
    'aside footer';
  min-height: 100vh;
}
header {
  grid-area: header;

  display: flex;
  justify-content: flex-end;
  padding: 1.5rem;
}
footer {
  grid-area: footer;
  background-color: #eeeeee;

  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 3rem;
}
aside {
  grid-area: aside;
  border-right: #eeeeee 1px solid;
  box-shadow: 0 0 10px 0 #eeeeee;

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding-top: 1.5rem;
  padding-bottom: 1.5rem;
}
main {
  grid-area: main;
  min-height: 80%;
  padding: 2rem;
}
</style>