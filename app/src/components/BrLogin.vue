<script setup lang="ts">
import { ref } from 'vue'
import type { Ref } from 'vue';

const user: Ref<string> = ref('');
const password: Ref<string> = ref('');
const saveInfo: Ref<boolean> = ref(false);

</script>
<template>
    <div id="container-root">
        <div class="container-image">
            <img src="@/assets/images/img-teste.svg" alt="">
        </div>
        <div class="container-form">
            <form>
                <div class="headers">
                    <span>Bem-vindo de volta</span>
                    <h1>Faça login na sua conta</h1>
                </div>
                <div class="inputs">
                    <div class="email">
                        <label>E-mail</label>
                        <input type="text" v-model="user" placeholder="exemplo@gmail.com"></input>
                    </div>
                    <div class="password">
                        <label>Password</label>
                        <input type="password" v-model="password" placeholder="0123456789"></input>
                    </div>
                    <div class="save-recover">
                        <div class="save">
                            <input type="radio" v-model="saveInfo">
                            <label>Lembre de mim</label>
                        </div>
                        <span>Esqueceu sua senha ?</span>
                    </div>
                </div>
                <div class="buttons">
                    <button type="submit" class="enter">Entrar na conta</button>
                    <button class="google">Ou faça login com o Google</button>
                </div>
                <span>Não tem uma conta? Cadastre-se</span>
            </form>
        </div>
    </div>
    
</template>
<style scoped>
* {
    font-family: 'Archivo';
}
#container-root {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: 100vh;
}
.container-image {
    display: flex;
    justify-content: center;
    width: 100%;;
    background-color: #F3FFF2;
}
.container-image img {
    width: 75%;
}
.container-form {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
}
.headers {
    display: flex;
    flex-direction: column;
    gap: 12px;
}
.container-form form {
    display: flex;
    flex-direction: column;
    gap: 40px;
}
.inputs {
    display: flex;
    flex-direction: column;
    gap: 24px;
}
.email, .password {
    display: flex;
    flex-direction: column;
    gap: 8px;

    label {
        font-size: 18px;
    }
}
input[type="text"],
input[type="password"] {
    width: 400px;
    height: 49px;
    border-radius: 4px;
    border: 1px solid #E8E8E8;
    padding: 16px;
    background-color: #F7FAFC;
}
.save-recover {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    span {
        color: #1E9E6A;
    }
}
.save {
    display: flex;
    gap: 12px;
}
.buttons {
    display: flex;
    flex-direction: column;
    gap: 24px;

    button {
        height: 52px;
    }

    .enter {
        color: #ffffff;
        background-color: #1E9E6A;
        border: 1px solid #1E9E6A;
        border-radius: 4px;
    }

    .google {
        color: #ffffff;
        background-color: #1A202C;
        border: 1px solid #1A202C;
        border-radius: 4px;
    }
}
</style>