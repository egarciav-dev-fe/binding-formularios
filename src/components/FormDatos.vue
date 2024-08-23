<script>
export default {
  name: 'FormDatos',
  data() {
    return {
      tarjeta: {
        tituloTarjeta: '',
        chip: '',
        numeroTarjeta: '',
        fechaExpiracion: '',
        propietarioTarjeta: '',
        tipoTarjeta: ''
      }
    }
  }
}
</script>
<template>
  <div id="app">
    <form>
      <div>
        <label for="tituloTarjeta">Título de la tarjeta: </label>
        <input id="tituloTarjeta" type="text" v-model.lazy="tarjeta.tituloTarjeta" />
      </div>

      <div>
        <label for="chip">Chip SRC: </label>
        <input id="chip" type="text" v-model="tarjeta.chip" />
      </div>

      <div>
        <label for="numeroTarjeta">Número: </label>
        <input id="numeroTarjeta" type="text" v-model.lazy="tarjeta.numeroTarjeta" />
      </div>

      <div>
        <label for="fechaExpiracion">Fecha de expiración: </label>
        <input id="fechaExpiracion" type="text" v-model.lazy="tarjeta.fechaExpiracion" />
      </div>

      <div>
        <label for="propietarioTarjeta">Propietario: </label>
        <input id="propietarioTarjeta" type="text" v-model.lazy="tarjeta.propietarioTarjeta" />
      </div>

      <div>
        <label for="tipoTarjeta">Tipo de tarjeta SRC: </label>
        <input id="tipoTarjeta" type="text" v-model="tarjeta.tipoTarjeta" />
      </div>
    </form>

    <div class="carnet">
      <h3>{{ tarjeta.tituloTarjeta }}</h3>
      <img width="40" :src="tarjeta.chip" alt="" />
      <div>
        <h2>{{ tarjeta.numeroTarjeta }}</h2>
        <span
          >Fecha Exp: <b>{{ tarjeta.fechaExpiracion }}</b></span
        >
      </div>
      <footer>
        <span>{{ tarjeta.propietarioTarjeta }}</span>
        <img :src="tarjeta.tipoTarjeta" width="60" />
      </footer>
    </div>
  </div>
</template>
<style scoped>
#app {
  display: flex;
  gap: 40px;
}
form {
  padding: 18px;
  border-radius: 20px;
  border: ridge 1px;
  box-shadow: 1px 1px 1px 1px gray;
  font-weight: bold;
  display: flex;
  flex-direction: column;
  gap: 15px;
  justify-content: center;
}
form div {
  display: grid;
  grid-template-columns: 100px 200px;
  align-items: center;
  gap: 5px;
}

form div label {
  text-align: right;
}

.carnet {
  width: 400px;
  height: 230px;
  background: #1c1a1e;
  color: white;
  border-radius: 20px;
  padding: 20px;
  box-shadow: 0px 0px 10px 2px black;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

h3 {
  font-size: 20px;
}

h2 {
  font-size: 30px;
  letter-spacing: 10px;
  margin-bottom: 15px;
  text-shadow: 0px 0px 1px gold;
  font-family: Times;
}

b {
  font-size: 16px;
}

footer {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  font-weight: bold;
  font-size: 18px;
  text-transform: uppercase;
  font-style: italic;
}
</style>
