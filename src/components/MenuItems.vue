<template>
    <div>
        <h1>testing</h1>
        <input  ref="user_data2"><br><br>
       
        <button @click="user_entered">items showing equal or less than above price
        </button>
        <section class="{menu_container}">
            <!-- use v-for -->
            <div v-for="(item, index) in items" :key="index">
                <article v-if="user_data>=item.price ">
                <h3>{{item.title}}</h3>
                <h3>{{item.price}}</h3>
                <h3>{{item.description}}</h3>
                <img :src="item.image_url">
                </article>
                
            </div>
        </section>
    </div>
</template>

<script>

    export default {
        name: 'menu-items',
        methods: {
            user_entered() {
                this.user_data = this.$refs.user_data2.value
            }
        },
      
       data: function() {
        return {
        /*{} for object inside array */ items: [{   
            title: 'fruits',
            price: 15,
            description: 'very juicy',
            image_url: 'https://images.unsplash.com/photo-1621961048737-a9993789e1ad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8d2F0ZXJtZWxvbnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
            },
            {   
            title: 'fruits_2',
            price: 13,
            description: 'very juicy 2',
            image_url: 'https://images.unsplash.com/photo-1621961048737-a9993789e1ad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8d2F0ZXJtZWxvbnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
            },
                        {   
            title: 'fruits_3',
            price: 5,
            description: 'very juicy 3',
            image_url: 'https://images.unsplash.com/photo-1621961048737-a9993789e1ad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8d2F0ZXJtZWxvbnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
            },
                        {   
            title: 'fruits_4',
            price: 8,
            description: 'very juicy 4',
            image_url: 'https://images.unsplash.com/photo-1621961048737-a9993789e1ad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8d2F0ZXJtZWxvbnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
            },
                        {   
            title: 'fruits_5',
            price: 11,
            description: 'very juicy 5',
            image_url: 'https://images.unsplash.com/photo-1621961048737-a9993789e1ad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8d2F0ZXJtZWxvbnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
            }
        ],
        menu_container: true,
        user_data: "abc"
        }
       }
    }
 
</script>

<style scoped>
.menu_container {
    background-color: gray;
}
</style>