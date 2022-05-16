<template>
  <main class="form-signin container">
  <form class="container">
      <img alt="Vue logo" src="../assets/logo.png">
    <h1 class="h3 mb-3 fw-normal">Please sign in</h1>

    <div class="form-floating">
      <input
        ref="telefono"
        type="tel" 
        class="form-control" 
        id="floatingInput" 
        placeholder="name@example.com"
        @keyup="validatePhone"
        >
      <label for="floatingInput">Telefono</label>
    </div>
    <div class="form-floating">
      <input type="password" class="form-control" id="floatingPassword" placeholder="Password">
      <label for="floatingPassword">Password</label>
    </div>

    <div class="checkbox mb-3">
      <label>
        <input type="checkbox" value="remember-me"> Remember me
      </label>
    </div>
    <button class="w-100 btn btn-lg btn-primary" type="submit">Sign in</button>
    <p class="mt-5 mb-3 text-muted">© 2017–2021</p>
  </form>
</main>
</template>

<script>
import { ref } from 'vue';

export default {
    name: "FormUser",

    setup(){
        const telefono = ref(null)
        function validatePhone(e){
            e.tsrget.value.replace(e.target.value, '')
        }
        return{
            validatePhone,
            telefono
        }
    }
}
</script>

<style>

</style>