<!--
 * @Author: zhangweiyuan-Royal
 * @LastEditTime: 2021-09-17 20:04:05
 * @Description: 
 * @FilePath: /my-vue-app/src/components/apps/Powerby.vue
-->
<template>
    <div>Loading</div>
</template>
<script lang="ts" setup>

import type { PageItem } from 'vue3-win10'
import { WindowIPC } from 'vue3-win10'
import type { PropType } from "vue"

let props = defineProps({
    ctx: {
        type: Object as PropType<PageItem>
    }
})
setTimeout(() => {
    window.open('https://webify.cloudbase.net/')
})
setTimeout(() => {
    if (props.ctx?.id) {
        WindowIPC.getInstance().destoryWindow(props.ctx?.id)
    }
},1000)


</script>

<style scoped>
.t2 {
    z-index: 99;
    background-color: blanchedalmond;
}
.t2:hover {
    background-color: rgba(255, 235, 205, 0.747);
}
</style>