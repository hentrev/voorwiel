<template>
  <v-btn
    rounded
    x-large
    color="success"
    to="rent"
  >
    <v-icon>mdi-bike</v-icon>&nbsp;<span>{{ buttonText }}</span>
  </v-btn>
</template>

<script>
  import { mapState } from 'vuex';

  export default {
    data() {
      return {}
    },
    computed: {
      buttonText() {
        return this.rents.length === 0 ? this.$t('message.rentbutton.rent-bike') : this.$t('message.rentbutton.rent-or-return-bike');
      },

      ...mapState(['rents'])
    },
  };
</script>
