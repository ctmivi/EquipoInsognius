<template>
  <form @submit.prevent="login" class="login-form">
    <div class="login">
      <div class="field">
        <label for="username" class="label">Username:</label>
        <div class="control">
          <input type="text" id="username" v-model="username" class="input" required>
        </div>
      </div>
      <div class="field">
        <label for="password" class="label">Password:</label>
        <div class="control">
          <input type="password" id="password" v-model="password" class="input" required>
        </div>
      </div>
      <div class="field is-grouped">
        <div class="control">
          <button type="submit" class="button is-primary">Iniciar Sesión</button>
        </div>
        
      </div>
      <div class="control">
          <router-link to="/register" class="button is-link">Regitrarse</router-link>
      </div>
    </div>
    
  </form>
</template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: ''
      };
    },
    methods: {
      login() {
        // Aquí puedes agregar la lógica para enviar los datos del formulario al servidor
        console.log('Username:', this.username);
        console.log('Password:', this.password);
      }
    }
  };
  </script>
  
  <style scoped>
@import '../../node_modules/bulma/css/bulma.css';  
/* Agrega tus estilos personalizados aquí, si es necesario */

  

  .login {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 10px;
    background-color: #fff;
    padding: 20px;
    border-radius: 30px;
    box-shadow: 0 0 40px rgba(255, 0, 0, 0.1);
    max-width: 400px;
    width: 100%;
    text-align: center;
  }
  
  .login-form{
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .form-group {
    margin-bottom: 10px;
  }
  
  button {
    margin-top: 10px;
  }
  </style>

  
  