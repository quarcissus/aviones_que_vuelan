<template>
  <div>
  <b-navbar toggleable="sm" type="dark" variant="dark">
    <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>

    <b-navbar-brand>Aviones que Vuelan</b-navbar-brand>

    <b-collapse id="nav-text-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#">Comprar vuelo</b-nav-item>
        <b-nav-item href="#">Consultar vuelo</b-nav-item>
        <b-nav-item href="#">Cancelar vuelo</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
  <div>
    <b-jumbotron class="jumbo-image" header="Aviones que vuelan" text-variant="white" lead="La mejor compañia para agendar tus vuelos">
      <p>Con nosotros no solo volaras tu</p>
      <b-button variant="outline-light" href="#">Agendar vuelo</b-button>
    </b-jumbotron>
  </div>
  <section>
    <b-container fluid>
      <b-row>
        <b-col cols="4">
          <div>
            <b-tabs content-class="mt-3">
              <b-tab title="Comprar vuelo" active>
                <label for="">¿A donde deseas viajar? </label>
                <b-form-input v-model="place" placeholder="¿A donde deseas viajar?"></b-form-input>
                <label for="">¿En que fecha deseas viajas?</label>
                <b-form-input v-model="date" placeholder="¿En que fecha deseas viajas?"></b-form-input>
                <b-button block variant="outline-dark">Conseguir un vuelo</b-button>
              </b-tab>
              <b-tab title="Cambiar vuelo">
                <label for="">Ingrese su ID de vuelo</label>
                <b-form-input v-model="id_cambiar" placeholder="ID vuelo"></b-form-input>
              </b-tab>
              <b-tab title="Cancelar vuelo">
                <label for="">Ingrese su ID de vuelo</label>
                <b-form-input v-model="id_cancelar" placeholder="ID vuelo"></b-form-input>
              </b-tab>
            </b-tabs>
          </div>
         
        </b-col>
        <b-col cols="8">
          <b-jumbotron class="tab-image" header="Consigue tu vuelo" text-variant="white" lead="">
            <p>Preparate para la mejor experiencia de vuelo</p>
          </b-jumbotron>
        </b-col>
      </b-row>
    </b-container>
  </section>
</div>
</template>

<script>

export default {
  data(){
    return {
      place:'',
      date:'',
      isModal: false,
      id_cambiar: '',
      id_cancelar: ''
    }

  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.jumbo-image{
  background: url("https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRQrfunHONLwS_stV5XkYYXUL5O_9lE569OSjcNaEyLf_DXOcZ-") no-repeat center center;
  -webkit-background-size: 100% 300%;
  -moz-background-size: 100% 300%;
  -o-background-size: 100% 300%;
  background-size: 100% 300%;
}

.tab-image{
  background: url("https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSQ1zSIWYNXTxsQcO5LtXdu3rK49e288UZzTAAOu0ZNgnfEfwWx") no-repeat center center;
  -webkit-background-size: 100% 300%;
  -moz-background-size: 100% 300%;
  -o-background-size: 100% 300%;
  background-size: 100% 300%;
}
</style>
