<script setup>
import { useUserStore } from '../store/user.js';
import UsersTable from './components/UsersTable.vue';
import CreateUserForm from './components/CreateUserForm.vue';

const { fetchUsers } = useUserStore();

try {
  fetchUsers();
} catch (error) {
  console.error('Error fetching users:', error);
}


</script>

<template>
  <div class="container">
    <UsersTable/>
    <CreateUserForm/>
  </div>

</template>

<style scoped>

</style>
