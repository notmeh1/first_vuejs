<template>
  <div class="container">
    <h1 class="text-center">Tabla de Usuarios</h1>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido</th>
          <th scope="col">RUN</th>
          <th scope="col">Nacimiento</th>
          <th scope="col">Edad</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(persona, $index) of personas" :key="$index">
          <th scope="row">{{ $index }}</th>
          <td>{{ persona.nombre }}</td>
          <td>{{ persona.apellido }}</td>
          <td>{{ persona.run }}</td>
          <td>{{ persona.nacimiento }}</td>
          <td>{{ persona.edad }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    personas: [
      {
        nombre: "Jose",
        apellido: "Pérez",
        run: "123456-2",
        nacimiento: "12-04-67",
        edad: 52,
      },
      {
        nombre: "María",
        apellido: "Rodríguez",
        run: "654321-1",
        nacimiento: "30-11-90",
        edad: 29,
      },
      {
        nombre: "Manuel",
        apellido: "Patiño",
        run: "14223456-6",
        nacimiento: "02-12-59",
        edad: 60,
      },
    ],
  }),
};
</script>

<style></style>
