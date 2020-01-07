<template>
<div id="app">
  <v-app id="inspire">
    <v-form>
      <v-container>
        <v-row>
          <v-col cols="12" sm="8" md="2">
            <v-text-field
              v-model.number="a"
              label="a"
              solo
              dense
            ></v-text-field>
          </v-col>
          <v-col cols="12" sm="8" md="1">
           <v-data><center>+</center></v-data>
          </v-col>           
          <v-col cols="12" sm="8" md="2">
            <v-text-field
              v-model.number="b"
              label="b"
              solo
              dense
            ></v-text-field>
          </v-col>
          <v-col cols="12" sm="8" md="1">
           <v-data><center>=</center></v-data>
          </v-col>   
          <v-col cols="12" sm="8" md="2">
            <v-text-field
              v-model="c"
              label="c"
              solo
              dense
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col class="text-center" cols="12" sm="8" md="8">
            <div>
              <v-btn depressed color="primary" v-on:click="add" large>Add</v-btn>
            </div>
        </v-col>
        </v-row>
      </v-container>
    </v-form>
  </v-app>
</div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  el: "#app",
  data: () => ({
    a: 0,
    b: 0,
    c: 0 
  }),
  methods: {
    add: function () {
        this.c =  this.a + this.b;
    }
  }
});
</script>
