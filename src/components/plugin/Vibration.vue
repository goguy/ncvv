// Require Cordova plugin : cordova-plugin-vibration

<template>
  <v-container text-center>
    <v-btn v-on:click="doVibrate">{{$t("startVibration")}}</v-btn>
  </v-container>
</template>

<script>
export default {
  name: 'vibration',
  methods: {
    doVibrate () {
      if (navigator.vibrate) {
        navigator.vibrate([100, 30, 100, 30, 100, 200, 200, 30, 200, 30, 200, 200, 100, 30, 100, 30, 100])
      } else {
        console.error('[cordova-plugin-vibration] Is required to use this function')
      }
    }
  }
}
</script>
