<template>
  <v-app>
    <v-navigation-drawer v-model="drawer">
      <v-list color="transparent">
        <v-list-item
          prepend-avatar="https://logopond.com/logos/7f16253b89ef051ea84faa28a114d4ce.png"
          title="Omnichannel"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-view-dashboard"
          title="Dashboard"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-account-box"
          title="Account"
        ></v-list-item>
        <v-list-item prepend-icon="mdi-gavel" title="Admin"></v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Painel de configuração</v-toolbar-title>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data: () => ({ drawer: null }),
};
</script>
