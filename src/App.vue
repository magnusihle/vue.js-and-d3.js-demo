<template>
  <v-app>
    <v-container>
      <v-col cols="12" sm="3">
        <v-btn v-if="$vuetify.theme.dark" text icon color="yellow" @click.stop="$vuetify.theme.dark = !$vuetify.theme.dark">
          <v-icon>mdi-weather-sunny</v-icon>
        </v-btn>
        <v-btn v-else text icon color="#1c2321" @click.stop="$vuetify.theme.dark = !$vuetify.theme.dark">
          <v-icon>mdi-weather-night</v-icon>
        </v-btn>
      </v-col>
    </v-container>
    <v-content>
      <v-container>
        <router-view></router-view>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
  })
};
</script>
<style lang="scss" scoped>
$dark-bg: #1c2321;

body {
  background-color: $dark-bg;
}
</style>
