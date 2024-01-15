<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="10">
        <v-card class="elevation-6 mt-10">
          <v-window v-model="step">
            <v-window-item :value="1">
              <v-row>
                <v-col cols="12" sm="6">
                  <v-card-text class="mt-12">
                    <h4 class="text-center">Faça login na sua conta</h4>
                    <h6 class="text-center grey--text">Faça login em sua conta para poder continuar<br>
                      e editar seus fluxos de integração
                    </h6>
                    <v-row align="center" justify="center">
                      <v-col cols="12" sm="8">
                        <v-text-field label="Email" outlined dense color="blue" autocomplete="false" class="mt-16"></v-text-field>
                        <v-text-field label="Senha" outlined dense color="blue" autocomplete="false" type="password"></v-text-field>
                        <v-row>
                          <v-col cols="12" sm="7">
                            <v-checkbox label="Lembrar-me" class="mt-n1" color="blue"></v-checkbox>
                          </v-col>
                          <v-col cols="12" sm="5">
                            <span class="caption blue--text">Esqueci a senha</span>
                          </v-col>
                        </v-row>
                        <v-btn color="blue" dark block tile>Log in</v-btn>
                        <h5 class="text-center grey--text mt-4 mb-3">Ou faça login usando</h5>
                        <div class="d-flex justify-space-between align-center mx-10 mb-16">
                          <v-btn depressed outlined color="grey">
                            <v-icon color="red">fab fa-google</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="blue">fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="light-blue lighten-3">fab fa-twitter</v-icon>
                          </v-btn>
                        </div>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-col>
                <v-col cols="12" sm="6" class="blue rounded-bl-xl" >
                  <div style="text-align:center; padding: 180px 0;">
                    <v-card-text class="white--text">
                      <h3 class="text-center">Ainda não tem uma conta?</h3>
                      <h6 class="text-center">
                        Vamos preparar tudo para que você possa começar a criar sua primeira<br>
                        experiência de integração
                      </h6>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step++">ASSINAR</v-btn>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
            <v-window-item :value="2">
              <v-row>
                <v-col cols="12" md="6" class="blue rounded-br-xl">
                     <div style="  text-align: center; padding: 180px 0;">
                      <v-card-text class="white--text" >
                        <h3 class="text-center ">Já se registrou?</h3>
                        <h6
                          class="text-center"
                        >Faça login na sua conta para poder continuar criando e editando seus fluxos de integração</h6>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn tile outlined dark @click="step--">Fazer login</v-btn>
                      </div>
                      </div>
                    </v-col>
                <v-col cols="12" sm="6">
                  <v-card-text class="mt-12">
                    <h4 class="text-center">Registrar-se em uma conta</h4>
                    <h6 class="text-center grey--text">
                      Vamos preparar tudo para que você possa começar a criar sua <br>
                      primeira experiência de integração
                    </h6>
                    <v-row align="center" justify="center">
                      <v-col cols="12" sm="8">
                        <v-row>
                          <v-col class="12" sm="6">
                            <v-text-field label="Primeiro nome" outlined dense color="blue" autocomplete="false" class="mt-4"></v-text-field>
                          </v-col>
                          <v-col class="12" sm="6">
                            <v-text-field label="Sobrenome" outlined dense color="blue" autocomplete="false" class="mt-4"></v-text-field>
                          </v-col>
                        </v-row>
                        <v-text-field label="Email" outlined dense color="blue" autocomplete="false"></v-text-field>
                        <v-text-field label="Senha" outlined dense color="blue" type="password"></v-text-field>
                        <v-row>
                          <v-col cols="12" sm="7">
                            <v-checkbox label="Eu aceito AAE" class="mt-n1" color="blue"></v-checkbox>
                          </v-col>
                          <v-col cols="12" sm="5">
                            <span class="caption blue--text ml-n4">Termos e condições</span>
                          </v-col>
                        </v-row>
                        <v-btn color="blue" dark block tile>Registrar-se</v-btn>
                        <h4 class="text-center grey-text mt-4 mb-3O">Ou registre-se usando</h4>
                        <div class="d-flex justify-space-between align-center mx-10 mb-11">
                          <v-btn depressed outlined color="grey">
                            <v-icon color="red">fab fa-google</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="blue">fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="light-blue lighten-3">fab fa-twitter</v-icon>
                          </v-btn>
                        </div>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-col>
              </v-row>
            </v-window-item>
          </v-window>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

  export default {
    data: () => ({
      step: 1
    }),
    props: {
      source: String
    }
    
  }
</script>
<style scoped>
  .v-application .rounded-bl-xl {
    border-bottom-left-radius: 300px !important;
  }
  .v-application .rounded-br-xl {
    border-bottom-right-radius: 300px !important;
  }
</style>