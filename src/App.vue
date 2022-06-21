<template>
  <v-app>
    <v-overlay :value="isLoading">
      <v-progress-circular indeterminate size="64" />
    </v-overlay>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    isLoading: true,
  }),
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 100000);
  },
};
</script>
