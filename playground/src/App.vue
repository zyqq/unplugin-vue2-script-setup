<script setup lang="ts">
import { defineAsyncComponent } from '@vue/composition-api'

import HelloWorld from './HelloWorld.vue'

const AsyncComponent = defineAsyncComponent(() => import('./Async.vue'))

function onUpdate(e: any) {
  // eslint-disable-next-line no-console
  console.log(e)
}
</script>
<template>
  <div>
    <HelloWorld name="Vue 2" @update="onUpdate" />

    <AsyncComponent />
  </div>
</template>
