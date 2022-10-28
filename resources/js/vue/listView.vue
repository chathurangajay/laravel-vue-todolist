<template>
    <div>
        <div v-for="(item, index) in items" :key="index" >
            <litst-item
                :item="item"
                class="item"
                v-on:itemchanged="$emit('reloadlist')"
            />
        </div>
    </div>
</template>

<script>
import litstItem from "./listItem.vue"

export default {
    props: ['items'],
    components: {
        litstItem
    }
}
</script>

<style scoped>
.item{
    background: #e6e6e6;
    padding: 5px;
    margin-top: 5px;
}
</style>