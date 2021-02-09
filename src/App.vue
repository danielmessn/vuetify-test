<template>
 <v-app>

   <v-navigation-drawer app
      v-model="drawer"
      absolute
      temporary
      right
   >
        <!-- Menu Links -->
        <v-list>
          <v-list-item to="/" exact>
            <v-list-item-action>
              <v-icon>mdi-home</v-icon>
            </v-list-item-action>
            <v-list-item-content>Home</v-list-item-content>
          </v-list-item>
          <v-list-item to="/about">
            <v-list-item-action>
              <v-icon>mdi-information</v-icon>
            </v-list-item-action>
            <v-list-item-content>About</v-list-item-content>
          </v-list-item>
        </v-list>

  </v-navigation-drawer>

  <v-app-bar clipped-right app>
     <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
  </v-app-bar>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container fluid>

      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

  <v-footer app>
    <!-- -->
  </v-footer>
  </v-app>
</template>

<script>

export default {
    name: "App",
     data: () => ({
      drawer: false,
    }),
  };
</script>
