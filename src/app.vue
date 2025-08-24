<template>
    <div id="app">
        {{ count }}
        <button @click="increment">+1</button>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import * as _ from "lodash";

export default defineComponent({
    name: 'App',
    data() {
        return {
            count: 0
        };
    },
    methods: {
        increment() {
            this.count++;
            console.log(_.ceil(this.count / 5));
        }
    }
});
</script>

<style lang="less" scoped>
#app {
    text-align: center;
    padding: 20px;

    button {
        margin-left: 10px;
        padding: 5px 10px;
    }
}
</style>