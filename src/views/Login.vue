<template>
    <section class="login-container">
        <h1>Welcome back to ezezimali</h1>
        <br>
        <form @submit.prevent="login" class="login-form">
            <label for="username">Username:</label>
            <input type="text" id="username" v-model="username" required>
            <label for="password">Password:</label>
            <input type="password" id="password" v-model="password" required>
            <button type="submit">Login</button>
        </form>
        <br>
        <article id="RegisterCTA">
            <h3>Dont have an account yet? </h3>
            <RouterLink to="/register">Register</RouterLink>

        </article>
    </section>
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
            // Perform login logic here
            // For simplicity, let's just assume login is successful
            // and navigate to the next page
            this.$router.push('/next-page');
        }
    }
};
</script>

<style scoped>
#RegisterCTA {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
    width: 18rem;

}

.login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
}

.login-form {
    width: 300px;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f9f9f9;
}

.login-form label {
    display: block;
    margin-bottom: 5px;
}

.login-form input {
    width: 100%;
    padding: 8px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 3px;
}

.login-form button {
    width: 100%;
    padding: 10px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 3px;
    cursor: pointer;
}

.login-form button:hover {
    background-color: #0056b3;
}
</style>