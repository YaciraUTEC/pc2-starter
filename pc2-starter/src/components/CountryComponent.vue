<script>
export default {
  name: "CountryComponent",
  props: [
    "name",
    "capital",
    "currency_name",
    "currency",
    "region",
    "code",
    //TODO: crear una propiedad para determinar si al componente se le puede hacer click
  ],
  monunted(){
    console.log("",this.$props.name)},//propiedad creada para acceder a los componentes de la propiedad
  methods:{
    showMessage(){
      alert("Al componente si se le puede hacer click");
    }
  }
}

</script>

<template>
  <!--TODO: Utilizar la propiedad creada para controlar el click. Cuando el componente es "clickeable", redirigir a la pagina del pais.
  Mira las rutas para ver como redirigir al usuario.-->
 
  <div>Componente{{name}}</div>
  <div>
    <button v-on:click="showMessage ">Click</button>
 
  <!--TODO: Poblar el HTML con las propiedades. Usar https://countryflagsapi.com/png/${code}-->
    <h1>Name: {{name}}</h1><br>
    <p>Capital: {capital}}</p><br>
    <p>Moneda: {{currency_name}} {{currency}}</p><br>
    <p>Region: {{region}}</p>
    <p>Code: {{code}}</p>
  <img 
      width="200"
      height="200"
      src = "https://countryflagsapi.com/png/${code}"
    />
    
  </div>
</template>

<style scoped>
.country {
  padding: 2px;
  white-space: nowrap;
  width: 350px;
  height: 350px;
  border-style: solid;
  border-radius: 5px;
  border-color: grey;
}

.country-hover:hover {
  background-color: rgb(49, 49, 49);
  cursor: pointer;
}

h1 {
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
