<template>
  <v-app>
    <!-- Barra padrao -->
    <v-app-bar color="primary">
      <v-btn icon @click="drawer = !drawer">
        <v-icon icon="mdi-menu">
        </v-icon>
      </v-btn>
      <v-app-bar-title>Cadastro de produtos </v-app-bar-title>
    </v-app-bar>

    <!-- Menu -->
    <v-navigation-drawer color="primary" v-model="drawer">
      <v-list-item to="/home" link prepend-icon="mdi-home-circle-outline">
        Home
      </v-list-item>

      <v-list-item  to="/produtos" prepend-icon="mdi-shopping">
        produtos
      </v-list-item>

      <v-list-item to="/sair" prepend-icon="mdi-logout">
        Sair
      </v-list-item>
    </v-navigation-drawer>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from 'vue'
const drawer = ref(false)
</script>
