<template>
    <q-page padding>
        <q-form v-on:keyup.enter="logar()" :model="fomularioLogin" ref="formularioLogin" class="q-gutter-md">
            <q-input filled lazy-rules type="email" v-model="fomularioLogin.email" label="Email"
                :rules="[val => val && val.length > 0 || 'Insira o E-mail']">
            </q-input>
            <q-input filled type="password" lazy-rules v-model="formularioLogin.senha" label="Senha"
                :rules="[val => val && val.length > 0 || 'Insira a senha']">
            </q-input>

            <div class="row justify-center content-center">
                <q-btn label="Logar" @click="logar()" color="primary">
                    <q-tooltip
                        transition-show="rotate"
                        transition-hide="rotate">
                        Logar!
                    </q-tooltip>
                </q-btn>

                <q-btn label="Limpar" @click="limpar()" color="primary" flar class="q-ml-sm">
                    <q-tooltip
                        transition-show="rotate"
                        transition-hide="rotate">
                        Limpar Formulário!
                    </q-tooltip>
                </q-btn>
            </div>
        </q-form>
    </q-page>
</template>

<script>
export default {
  data () {
    return {
      formularioLogin: {}
    }
  },
  methods: {
    logar () {

    },
    limpar () {
      this.formularioLogin = {}
    }
  },
  create () {
    console.log('Assim que a tela for iniciada essa mensagem irá aparecer')
  }
}
</script>
