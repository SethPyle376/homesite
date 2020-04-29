<template>
  <div>
    <v-app-bar dense dark app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Seth Pyle</v-toolbar-title>
      <v-spacer/>
      <v-btn icon>
        <v-icon>fab fa-github</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>fab fa-linkedin</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>fas fa-blog</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <v-list
        dense
        nav
        class="py-0"
      >
        <v-list-item two-line>
          <v-list-item-avatar>
            <img src="https://scontent-sjc3-1.xx.fbcdn.net/v/t1.0-1/p160x160/73213733_2777913255565461_2912588903066107904_n.jpg?_nc_cat=103&_nc_sid=dbb9e7&_nc_ohc=yUlMmpytZbcAX9Px3CV&_nc_ht=scontent-sjc3-1.xx&_nc_tp=6&oh=2ebd884f05f6af87916fe764b70b084b&oe=5ECFB44F">
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>Contact Me!</v-list-item-title>
            <v-list-item-subtitle>seth.pyle86@gmail.com</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
      </v-list>
    </v-navigation-drawer>
    <router-view/>
  </div>
</template>

<script>

export default {
  data: () => {
    return {
      drawer: false
    }
  }
}
</script>