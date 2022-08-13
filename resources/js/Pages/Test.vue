<script setup>
import BreezeAuthenticatedLayout from '@/Layouts/Authenticated.vue';
import { Head,Link } from '@inertiajs/inertia-vue3';
import { loadLanguageAsync } from 'laravel-vue-i18n';


</script>

<template>
    <Head title="Test" />

    <BreezeAuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                {{$t('Dashboard')}}
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-sm sm:rounded-lg">
                    <div class="p-6 bg-white border-b border-gray-200">
                        <Link href="/dashboard">go3ksjdf to dashboard</Link>
                          <button @click="loadLanguageAsync('zh_TW')">Change to zh_TW Language</button>
                          <span>haha{{$t('auth.failed')}}</span>
                    </div>
                </div>
            </div>
        </div>
    </BreezeAuthenticatedLayout>
</template>
