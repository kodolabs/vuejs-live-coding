<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="min-h-screen bg-gray-100">
    <header class="bg-white shadow">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <div class="flex">
            <div class="flex-shrink-0 flex items-center">
              <h1 class="text-xl font-bold text-gray-900">My App</h1>
            </div>
            <nav class="ml-10 flex items-center space-x-4">
              <RouterLink
                to="/dashboard"
                class="px-3 py-2 rounded-md text-sm font-medium"
                :class="$route.path === '/dashboard' ? 'bg-gray-900 text-white' : 'text-gray-700 hover:bg-gray-200'"
              >
                Dashboard
              </RouterLink>
              <RouterLink
                to="/reports"
                class="px-3 py-2 rounded-md text-sm font-medium"
                :class="$route.path === '/reports' ? 'bg-gray-900 text-white' : 'text-gray-700 hover:bg-gray-200'"
              >
                Reports
              </RouterLink>
            </nav>
          </div>
        </div>
      </div>
    </header>
    <main class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
      <RouterView />
    </main>
  </div>
</template>
