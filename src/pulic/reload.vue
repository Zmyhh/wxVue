<template>
    
</template>

<script>
    export default {
        name: "reload",
        created: function () {
            let url = window.location.href
            // this.url=url
            let a = url.indexOf('=')
            this.$cookies.set('wxtoken', url.substr(a + 1))
            if (this.$cookies.get('wxtoken')){
                this.$router.push('framework')
            }



        }
    }
</script>

<style scoped>
    .active {

        color: #00aaee;
    }
</style>