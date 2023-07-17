<script setup>
import { reactive } from 'vue'
const paciente = reactive({
  nombre: '',
  propietario: '',
  email: '',
  fecha: '',
  sintomas: ''
})

</script>

<template>
  <div class="md:w-1/2">
    <h2 class="font-black text-3xl text-center">Seguimiento Pacientes</h2>
    <p class="text-lg mt-5 text-center mb-10">Añade pacientes y <span class="text-indigo-600 font-bold">Adminístralos</span></p>

    <!-- Formulario -->
    <form class="bg-white shadow-md rounded-lg py-10 px-5 mb-10">
      <!-- Nombre -->
      <div class="mb-5">
        <label 
          for="mascota"
          class="block text-gray-700 uppercase font-bold mb-2"
        >
          Nombre Mascota
        </label>
        <input 
          type="text"
          id="mascota"
          placeholder="Nombre Mascota"
          class="border-2 w-full p-2 placeholder-gray-400 rounded-md"
          v-model="paciente.nombre"
        >
      </div>
      <!-- Propietario -->
      <div class="mb-5">
        <label 
          for="propietario"
          class="block text-gray-700 uppercase font-bold mb-2"
        >
          Nombre Propietario
        </label>
        <input 
          type="text"
          id="propietario"
          placeholder="Nombre Propietario"
          class="border-2 w-full p-2 placeholder-gray-400 rounded-md"
          v-model="paciente.propietario"
        >
      </div>
      <!-- Email -->
      <div class="mb-5">
        <label 
          for="email"
          class="block text-gray-700 uppercase font-bold mb-2"
        >
          Nombre Propietario
        </label>
        <input 
          type="email"
          id="email"
          placeholder="Email Propietario"
          class="border-2 w-full p-2 placeholder-gray-400 rounded-md"
          v-model="paciente.email"
        >
      </div>
      <!-- Fecha Alta -->
      <div class="mb-5">
        <label 
          for="alta"
          class="block text-gray-700 uppercase font-bold mb-2"
        >
          Fecha Alta
        </label>
        <input 
          type="date"
          id="alta"
          class="border-2 w-full p-2 placeholder-gray-400 rounded-md"
          v-model="paciente.fecha"
        >
      </div>
      <!-- Sintomas -->
      <div class="mb-5">
        <label 
          for="sintomas"
          class="block text-gray-700 uppercase font-bold mb-2"
        >
          Síntomas
        </label>
        <textarea 
          id="sintomas"
          placeholder="Describe los sintomas"
          class="border-2 w-full p-2 placeholder-gray-400 rounded-md h-40"
          v-model="paciente.sintomas"
          />
      </div>

      <input 
        type="submit" 
        value="Registrar Paciente"
        class="bg-indigo-600 w-full hover:bg-indigo-700 text-white uppercase font-bold p-3 rounded-md cursor-pointer transition-colors"
      >
    </form>
  </div>
</template>


