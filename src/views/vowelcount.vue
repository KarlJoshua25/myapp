<template >
    <div class=" justify-center mb-6">
      <v-card class="pa-15" max-width="544" color="white">
        <v-card-title> Vowel Counter </v-card-title>
  
        <v-text-field label="Enter a String" v-model="input1"></v-text-field>
  
        <v-card-actions>
          <v-btn color="primary" @click="doCountVowel"> Submit </v-btn>
        </v-card-actions>
  
        <h3>Vowels:</h3>
        {{ output1 }}
      </v-card>
    </div>
  </template>
  
  
  <script setup>
  import { ref } from "vue";
  const input1 = ref("");
  const output1 = ref(0);
 
  
  function doCountVowel() {
    output1.value = input1.value.match(/[aeiou]/gi).length;
   
  }
  </script>
  