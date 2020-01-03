<template>
    <div class="id">
        <h1>{{value}}</h1>
        <button v-on:click="update()">undate</button>
        <button c-on:click="destroyEvent">destroy</button>
    </div>
</template>
<script>
export default {
    name:'id',
    data(){
        return{
            value:'giá trị ban đầu '
        }
    },

    beforeCreate() {
        alert('beforeCreate!')
    },
    created(){
        alert('created')
    },
    beforeMount(){
        alert('beforeMount')
    },
    mounted(){
        alert('mounted')
    },
    beforeUpdate(){
        alert('beforeUpdate')
    },
    updated(){
        alert('updated')
    },
    beforeDestroy(){
        alert('beforeDestroy')
    },
    destroyed(){
        alert('destroyed')
    },
    methods:{
        destroyEvent: function(){
            this.$destroy();
        },
        update: function(){
               this.value = 'giá trị đã được update!!!!'
        }
    }

}
</script>
<style>

</style>