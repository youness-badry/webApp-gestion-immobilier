<template>
  <div class="home">
    <h1>Home</h1>
    <div class="users-list">
      <router-link v-for="user in users" :to="{ name: 'UserProfile', params: {userId: user.id}}" :key="user.id">
        {{user.username}} <br>
      </router-link>
    </div>
  </div>
</template>

<script>
import {users} from "@/assets/users";

export default {
  name: 'Home',
  setup() {
    return {
      users
    }
  }
}
</script>
