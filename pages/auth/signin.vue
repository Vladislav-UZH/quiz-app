<script setup lang="ts">
definePageMeta({ layout: "auth" });
</script>
<template>
  <UiBlock class="box">
    <div class="title-box">
      <h2>Log in to your account</h2>
      <p class="description">Welcome Back! Please enter your details.</p>
    </div>
    <form class="form">
      <UiField
        name="email"
        type="email"
        label="Email"
        placeholder="Enter Email"
      />
      <div>
        <UiField
          name="password"
          type="password"
          label="Password"
          placeholder="Create Password"
        />
        <!-- <nuxt-link to="/auth/recovery">Forgot password?</nuxt-link> -->
      </div>

      <UiButton>Start</UiButton>
    </form>
    <nuxt-link class="sign-up-link" to="/auth/signup">
      Don`t have an account? <span class="sign-up">Sign up</span>
    </nuxt-link>
  </UiBlock>
</template>

<style scoped>
.box {
  padding: 40px;
  display: flex;
  flex-direction: column;
  /* align-items: center; */
  gap: 32px;
}
.title-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
}
.form {
  display: flex;
  flex-direction: column;
  gap: 32px;
}
.description {
  text-align: center;

  color: var(--secondary-text-color);
}
.sign-up-link {
  color: var(--secondary-text-color);
  text-align: center;
}

.sign-up {
  color: var(--primary-accent-color);
  font-weight: 700;
}
</style>
