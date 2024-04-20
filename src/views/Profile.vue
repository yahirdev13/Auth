<template>
  <div class="profile-container">
    <img :src="user.picture" alt="User Picture" class="profile-picture">
    <h2 class="profile-name">{{ user.name }}</h2>
    <p class="profile-email">{{ user.email }}</p>
    <p class="profile-nickname">{{ user.nickname }}</p>
    <p class="profile-locale">{{ user.locale }}</p>
    <p class="profile-updated">{{ user.updated_at }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {},
    };
  },
  mounted() {
    this.user = this.$auth.user;
  },


};
</script>