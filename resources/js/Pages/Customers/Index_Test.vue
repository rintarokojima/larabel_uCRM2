<script setup>
import FlashMessage from '@/Components/FlashMessage.vue';
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/inertia-vue3';
import { onMounted } from 'vue';
import Pagination from '@/Components/Pagination.vue'


defineProps({
    customers: Object
})

// onMounted(() =>{
//     console.log(prpps.customers)
//     console.log(prpps.customers.last_page)

// })

</script>

<template>
    <ul v-for="customer in customers.data" :key="customer.id"> <li>{{ customer.id }}</li>
    <li>{{ customer.name }}</li>
    </ul>
    <Pagination class="mt-6" :links="customers.links"></Pagination>
</template>
