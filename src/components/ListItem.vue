<template lang="html">
  <li v-on:click="handleClick">{{munro.name}}</li>
</template>

<script>
import { eventBus } from '../main.js' //curly braces because we only import eventbus not whole main.bus
export default {
  name: 'list-item',
  props: ['munro'],
  methods: {
    handleClick(){
      eventBus.$emit('munro-selected', this.munro)//$emit is a function.
    }
  }
}
</script>

<style lang="css" scoped>
</style>
