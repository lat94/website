<template>
    <master>
        <template slot="head">
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <title><slot name="title"/></title>
            <meta v-if="this.$slots.description" name="description" :content="this.$slots.description[0].text">
            <link href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,500,700&display=swap" rel="stylesheet">
            <!-- Favicon Files -->
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="apple-touch-icon" sizes="57x57" href="/apple-icon-57x57.png">
            <link rel="apple-touch-icon" sizes="60x60" href="/apple-icon-60x60.png">
            <link rel="apple-touch-icon" sizes="72x72" href="/apple-icon-72x72.png">
            <link rel="apple-touch-icon" sizes="76x76" href="/apple-icon-76x76.png">
            <link rel="apple-touch-icon" sizes="114x114" href="/apple-icon-114x114.png">
            <link rel="apple-touch-icon" sizes="120x120" href="/apple-icon-120x120.png">
            <link rel="apple-touch-icon" sizes="144x144" href="/apple-icon-144x144.png">
            <link rel="apple-touch-icon" sizes="152x152" href="/apple-icon-152x152.png">
            <link rel="apple-touch-icon" sizes="180x180" href="/apple-icon-180x180.png">
            <link rel="icon" type="image/png" sizes="192x192"  href="/android-icon-192x192.png">
            <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
            <link rel="icon" type="image/png" sizes="96x96" href="/favicon-96x96.png">
            <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
            <link rel="manifest" href="/manifest.json">
            <meta name="msapplication-TileColor" content="#ffffff">
            <meta name="msapplication-TileImage" content="/ms-icon-144x144.png">
            <meta name="theme-color" content="#ffffff">
            <!-- Favicon Files -->

            <slot name="head"/>
        </template>
        <template slot="body"><slot name="content"/></template>
    </master>
</template>
<style lang="stylus">
@import "~@/stylus/variables"


body
    background #eee
    font-family 'Roboto', sans-serif
    color mix($main, #000, 10%)

a
    text-decoration none 
    color $main
    font-weight 500

.flex
    display flex
    &.justify-center
        justify-content center

</style>
<script>
import master from "@/layouts/master"

export default {
    components: {
        master
    }
}
</script>