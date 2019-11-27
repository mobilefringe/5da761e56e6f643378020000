<template>
    <div v-if="property" class="main_container">
        <div class="message_content">
            <h1 class="center">{{ property.welcome_message }}</h1>
            <p class="center">{{ property.description }}</p> 
            <!--<p class="center">Pacific Pearl delivers the ultimate shopping experience in a distinctive outdoor setting. Immerse your shopping senses in a unique blend of specialty retailers and restaurants.</p>-->
        </div>
    </div>
</template>

<script>
    define(["Vue", "vuex"], function(Vue, Vuex){
        return Vue.component("messages-component", {
            template: template, // the variable template will be injected
            computed: {
                ...Vuex.mapGetters([
                    'property'
                ])
            }
        })
    });
</script>