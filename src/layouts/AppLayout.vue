<template>
  <div>
    <q-layout view="hHr LpR lFf" container style="height: 100vh">
      <q-header reveal elevated bordered class="bg-white">
        <q-toolbar class="bg-white text-black">
          <q-btn flat round dense icon="menu" @click="drawer = !drawer" />
          <q-toolbar-title> Echart-quasar-vue </q-toolbar-title>
          <q-btn flat round dense icon="apps" class="q-mr-xs" />
          <q-btn flat round dense icon="more_vert" />
        </q-toolbar>
        <q-drawer
          side="left"
          v-model="drawer"
          bordered
          :width="200"
          :breakpoint="500"
          content-class="bg-grey-3"
        >
          <q-list bordered class="text-black">
            <q-item clickable v-ripple>
              <q-item-section avatar>
                <q-icon color="primary" name="bluetooth" />
              </q-item-section>
              <q-item-section>Icon as avatar</q-item-section>
            </q-item>
          </q-list>
        </q-drawer>
        <router-view />
      </q-header>
    </q-layout>
  </div>
</template>

<script setup>
import { ref } from "vue";

const drawer = ref(true);
</script>

<style></style>
