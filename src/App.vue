<template>
    <div id="app">
        <Navigation v-if="currentUser"></Navigation>
    	<router-view/>
        Hello World 2
    </div>
</template>

<script>
    import { mapState } from 'vuex'
    import Navigation from './components/Navigation.vue'

    export default {
        components: { Navigation },
        computed: {
            ...mapState(['currentUser'])
        }
    }
</script>
