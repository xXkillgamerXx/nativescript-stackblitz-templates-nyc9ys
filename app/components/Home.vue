<template>
  <Page>
    <ActionBar title="ActionBar Title">
      <ActionItem
        @tap="onTapShare"
        ios.systemIcon="9"
        ios.position="left"
        android.systemIcon="ic_menu_share"
        android.position="actionBar"
      />
      <ActionItem
        @tap="onTapDelete"
        ios.systemIcon="16"
        ios.position="right"
        text="delete"
        android.position="popup"
      />p
    </ActionBar>

    <GridLayout>
      <Label
        class="text-xl align-middle text-center text-gray-500"
        :text="message"
        @tap="logMessage"
      />
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import Vue from 'nativescript-vue';

export default Vue.extend({
  computed: {
    message() {
      return 'Hola mundo';
    },
  },

  methods: {
    logMessage() {
      console.log('You have tapped the message!');
    },
    onTapDelete() {
      console.log('onTapDelete');
    },
    onTapShare() {
      console.log('onTapShare');
    },
  },
});
</script>

<style>
/* .info {
    font-size: 20;
  } */
</style>
