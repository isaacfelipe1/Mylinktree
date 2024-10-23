<template>
  <div class="linktree-container">
    <div class="profile-card">
      <img class="profile-image" :src="profileImage" alt="Profile Picture" />
      <h1>{{ profileName }}</h1>
      <p>{{ description }}</p>
      <div class="links">
        <a v-for="link in links" :key="link.name" :href="link.url" target="_blank" class="link-button">
          <img :src="link.icon" alt="Icon" />
          {{ link.name }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      profileImage: "../src/assets/perfi_Isaac.jpg", 
      profileName: "Isaac Felipe",
      description: "Bem-vindo ao meu LinkTree!",
      links: [
        {
          name: "GitHub",
          url: "https://github.com/isaacfelipe1",
          icon: "https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
        },
        {
          name: "LinkedIn",
          url: "https://www.linkedin.com/in/isaac-felipe/",
          icon: "https://cdn-icons-png.flaticon.com/512/174/174857.png"
        }
      ]
    };
  }
};
</script>

<style scoped>
.linktree-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #1f1f1f;
}

.profile-card {
  background-color: #3b3b3b;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  color: white;
}

.profile-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-bottom: 20px;
  border: 2px solid #6a1b9a;
}

h1 {
  font-size: 24px;
  margin: 10px 0;
}

p {
  font-size: 16px;
  margin-bottom: 20px;
}

.links {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.link-button {
  background-color: #484848;
  padding: 10px;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-decoration: none;
  font-size: 18px;
  transition: background-color 0.3s ease;
}

.link-button:hover {
  background-color: #6a1b9a;
}

.link-button img {
  width: 24px;
  height: 24px;
  margin-right: 10px;
}
</style>
