<template>
<div class="signup">
  <form action="">
      <label >Email</label>
      <input type="email" required v-model="email">

       <label > Password </label>
      <input type="password" required v-model="password">
      <label>Role</label>
      <select v-model="role">
          <option value="Developer">Web Developer</option>
          <option value="Designer">Web Designer</option>
      </select>
      <div>
          <input type="checkbox" v-model="terms">
          <label class="labelcheck">Accept The Terms And Conditions</label>
      </div>
  </form>
   <h2>Email: {{ email }} </h2>
   <h2> Password: {{password}}</h2>
   <h2> Role : {{ role }}</h2>
   <h2> Terms Accepted: {{terms}}</h2>
  </div>
</template>

<script>
export default {
data(){
    return{
        email:'',
        password:'',
        role:'Developer',
        terms:false
    }
}
}
</script>

<style>
.signup{
    width: 90%;
    margin: auto;
    height: fit-content;
}
form{
    max-width: 40rem;
    text-align: left;
    padding: 3rem;
    border-radius: 1rem;
    background: white;
    margin: auto;
}
label{
    color: #aaa;
    display: inline-block;
    margin: 1rem 0 1rem;
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.1rem;
    font-weight: bold;
}
input,select{
    display: block;
    padding: 1rem 0.4rem;
    width: 100%;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}
h2{
    padding-top: 2rem;
}
input[type="checkbox"]{
    display: inline-block;
    position: relative;
    top: 0.125rem;
    width:1rem;
    margin: 0rem 1rem 0rem 0rem;
}
</style>