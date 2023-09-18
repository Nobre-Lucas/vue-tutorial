<template>
    <button @click="onClick()" :style="{ background: color }" class="btn">{{ text }}</button>
</template>

<script>
export default {
    name: "Button",
    props: {
        text: {
            type: String,
            default: "Add Something",
        },
        color: {
            type: String,
            default: "Black",
        },
    },
    methods: {
        onClick() {
            this.$emit('btn-click')
        }
    },
    emits: ['btn-click']
};
</script>