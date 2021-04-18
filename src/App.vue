<template>
  <v-app>
    <v-app-bar
      app
      color="red"
      dark
    >
      
      <v-spacer></v-spacer>

      <v-menu
            top
            :close-on-click="closeOnClick"
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                icon
                v-bind="attrs"
                v-on="on"
              >
                <v-icon>mdi-account-circle</v-icon>
              </v-btn>
            </template>

            <v-list>
              <v-list-item
                v-for="(item, index) in  menuItems"
                :key="index"
              >
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>

    </v-app-bar>




    <v-main>

    <v-toolbar>

        <v-btn text >
          Menu 1
        </v-btn>

        <v-btn text >
              Menu 2
            </v-btn>

       </v-toolbar>

     

      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },




  data: () => ({
    //
    menuItems: [{title: 'Menu1'}, {title: 'Menu 2'}],


  }),
};
</script>
