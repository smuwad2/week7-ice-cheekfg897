<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
            
        },
        methods: {
            deleteItem(index){
                this.items.splice(index, 1)
            },
            submitItem(newItem){
                this.items.push(newItem)
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul >
        <li v-for="(item, index) in items" :key="index">
            {{ item }}
            <button @click="deleteItem(index)">Delete!</button>
        </li>
     </ul>
     <input v-model="newItem"></input>
     <button @click=submitItem(newItem)>Add!</button>
   
</template>
