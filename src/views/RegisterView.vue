<template>
<div class="form-wrap">
    <form class="register">
      <p class="login-register">
        Already have an account?
        <router-link class="router-link" :to="{ name: 'Login' }">Login</router-link>
      </p>
      <h2>Create Your Account</h2>
      <div class="inputs">
        <div class="input">
          <input type="text" placeholder="First Name" v-model="firstName" />
          <user class="icon" />
        </div>
        <div class="input">
          <input type="text" placeholder="Last Name" v-model="lastName" />
          <user class="icon" />
        </div>
        <div class="input">
          <input type="text" placeholder="Username" v-model="username" />
          <user class="icon" />
        </div>
        <div class="input">
          <input type="text" placeholder="Email" v-model="email" />
          <email class="icon" />
        </div>
        <div class="input">
          <input type="password" placeholder="Password" v-model="password" />
          <password class="icon" />
        </div>
        <div v-show="error" class="error">{{ this.errorMsg }}</div>
      </div>
      <button class="btn btn-dark btn-lg rounded-pill" @click.prevent="register">Sign Up</button>
      <div class="angle"></div>
    </form>
    <div class="background"></div>
  </div>
</template>

<script>
// import email from '../assets/Icons/envelope-regular.svg'
// import password from '../assets/Icons/lock-alt-solid.svg'

export default {
    name: "LoginView",
    components: {
        // email,
        // password,
    },
    data() {
        return {
            // email: null,
            // password: null
        }
    }
}
</script>

<!-- <style lang="scss" scoped>
.form-wrap {
  overflow: hidden;
  display: flex;
  height: 100vh;
  justify-content: center;
  align-self: center;
  margin: 0 auto;
  width: 90%;
  @media (min-width: 900px) {
    width: 100%;
  }
  .login-register {
    margin-bottom: 32px;
    .router-link {
      color: #000;
      text-decoration: underline;
    }
    .router-link:hover{
        text-decoration: none;
    }
  }

  form {
    padding: 0 10px;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 1;
    @media (min-width: 900px) {
      padding: 0 50px;
    }
    h2 {
      text-align: center;
      font-size: 32px;
      color: #303030;
      margin-bottom: 40px;
      @media (min-width: 900px) {
        font-size: 40px;
      }
    }
    .inputs {
      width: 100%;
      max-width: 350px;
      .input {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 8px;
        input {
          width: 100%;
          border: none;
          background-color: #dfdfdf;
          padding: 4px 4px 4px 30px;
          height: 50px;
          &:focus {
            outline: none;
          }
        }
        .icon {
          width: 12px;
          position: absolute;
          left: 6px;
        }
      }
    }
    .forgot-password {
      text-decoration: none;
      color: #000;
      cursor: pointer;
      font-size: 14px;
      margin: 16px 0 32px;
      border-bottom: 1px solid transparent;
      transition: 0.5s ease all;
      &:hover {
        border-color: #303030;
      }
    }
    .angle {
      display: none;
      position: absolute;
      background-color: rgb(218, 218, 218);
      transform: rotateZ(3deg);
      width: 60px;
      right: -30px;
      height: 101%;
      @media (min-width: 900px) {
        display: initial;
      }
    }
  }
  .background {
    display: none;
    flex: 2;
    background-size: cover;
    background-image: url("../assets/penguin.jpg");
    width: 100%;
    height: 100%;
    @media (min-width: 900px) {
      display: initial;
    }
  }
}
</style> -->