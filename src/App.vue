<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      dark
      app
      color="#0C2556 "
    >
      <v-list>

          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title class="text-h3 font-weight-black text-center">
                Lipr.
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          class="text--secondary"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-subheader>REPORTS</v-subheader>
      <v-list>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          class="text--secondary"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-bell-outline</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-cog-outline</v-icon>
      </v-btn>


      <v-menu
        left
        bottom
        offset-y
        :nudge-bottom="4"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
      <v-avatar
        size="42"
      >
      <img
        src="https://i.imgur.com/73L3A4W.png"
        alt="Your Company Name"
      >
    </v-avatar>
            <!-- <v-icon>mdi-chevron-down</v-icon> -->
          </v-btn>
        </template>

        <v-list>
          <v-list-item>
            <v-list-item-avatar>
              <img
                src="https://i.imgur.com/73L3A4W.png"
                alt="Your Company Name"
              >
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Company Name</v-list-item-title>
              <v-list-item-subtitle>Edit Profile</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <v-divider></v-divider>


        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: null,
    items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Analytics', icon: 'mdi-account-box' },
          { title: 'Customers', icon: 'mdi-account-group-outline' },
          { title: 'Payments', icon: 'mdi-credit-card-outline' },
          { title: 'Reports', icon: 'mdi-file-edit-outline' },
          { title: 'Marketing', icon: 'mdi-message-outline' },
          { title: 'Edit Profile', icon: 'mdi-account-edit-outline' },
          { title: 'Settings', icon: 'mdi-cog-outline' },
          { title: 'Contact Us', icon: 'mdi-phone-outline' },
          { title: 'Report a Problem', icon: 'mdi-alert' },
          { title: 'FAQs', icon: 'mdi-frequently-asked-questions' },
          { title: 'Terms & Conditions', icon: 'mdi-alert-circle-outline' },
        ]
  }),
};
</script>
