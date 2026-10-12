<template>
  <v-container class="h-full flex items-center" max-width="900">
    <div>
      <v-img
        alt="Placeholder logo"
        class="mb-4"
        height="150"
        src="@/assets/logo.png"
      />

      <div class="mb-8 text-center">
        <div class="font-light -mb-1">Welcome to</div>
        <h1 class="text-6xl font-heading font-bold">Vuetify</h1>
      </div>

      <v-row class="mt-5">
        <v-col
          ><v-btn><v-icon icon="mdi-arrow-left" />Left Aligned</v-btn></v-col
        >
        <v-col class="text-right"
          ><v-btn>Aligned to the Right <v-icon icon="mdi-arrow-right" /></v-btn
        ></v-col>
      </v-row>

      <v-row>
        <v-col cols="12" class="border-b py-4">
          <div class="flex items-center gap-4">
            <v-avatar
              icon="mdi-rocket-launch-outline"
              size="40"
              variant="tonal"
            />
            <div>
              <h2 class="my-0 text-lg font-medium">Get started</h2>
              <div class="leading-7">
                Change this page by updating
                <v-code>components/HelloWorld.vue</v-code>.
              </div>
            </div>
          </div>
        </v-col>

        <v-col cols="3" class="font-medium">Href</v-col>
        <v-col cols="3" class="font-medium">Icon</v-col>
        <v-col cols="3" class="font-medium">Subtitle</v-col>
        <v-col cols="3" class="font-medium">Title</v-col>
        <template v-for="link in links" :key="link.href">
          <v-col cols="3" class="break-all border-b py-4">
            <a :href="link.href" rel="noopener noreferrer" target="_blank">{{
              link.href
            }}</a>
          </v-col>
          <v-col cols="3" class="border-b py-4">
            <v-icon :icon="link.icon" />
          </v-col>
          <v-col cols="3" class="border-b py-4">{{ link.subtitle }}</v-col>
          <v-col cols="3" class="border-b py-4">{{ link.title }}</v-col>
        </template>
      </v-row>
    </div>
  </v-container>
</template>

<script setup lang="ts">
const links = [
  {
    href: "https://vuetifyjs.com/",
    icon: "mdi-text",
    subtitle: "Learn about all things Vuetify in our documentation.",
    title: "Documentation",
  },
  {
    href: "https://vuetifyjs.com/introduction/why-vuetify/#feature-guides",
    icon: "mdi-star",
    subtitle: "Explore available framework Features.",
    title: "Features",
  },
  {
    href: "https://vuetifyjs.com/components/all",
    icon: "mdi-widgets-outline",
    subtitle: "Discover components in the API Explorer.",
    title: "Components",
  },
  {
    href: "https://discord.vuetifyjs.com",
    icon: "mdi-account-group-outline",
    subtitle: "Connect with Vuetify developers.",
    title: "Community",
  },
];
</script>

<style scoped>
@reference "../styles/tailwind.css";
</style>
