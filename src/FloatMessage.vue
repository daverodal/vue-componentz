<template>
        <vue-draggable-resizable v-if="message" :resizable="false" :x="x" :y="y" v-on:dragging="onDrag" v-on:resizing="onResize" style="z-index:300;" :parent="true">
            <header>
                {{header}}
            </header>
            <p v-html="message">
            </p>
        </vue-draggable-resizable>
</template>

<script>
    import VueDraggableResizable from 'vue-draggable-resizable'

    export default {
        props: ["message","header", "x", "y"],
        data: function () {
            return {
            }
        },
        methods: {
            onResize: function (x, y, width, height) {

            },
            onDrag: function (x, y) {

            }
        }
    }
</script>
<style lang="scss">
    #myFloater {
        padding:5px;
        header{
            font-size:30px;
        }
        height: auto !important;
        width: auto !important;
        background: fuchsia;

        /*white-space: nowrap;*/
        /*position: absolute;*/
        /*display: none;*/
        background: rgba(255, 255, 255, .9);
        border-radius: 10px;
        border: 2px solid black;
        box-shadow: 10px 10px 10px rgba(30, 30, 30, .85);
        z-index: 4;
        cursor: move;
    }
</style>