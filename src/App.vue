<script setup>
import { ref } from 'vue';
import { useToast } from "primevue/usetoast";

const text = ref();
const toast = useToast();
const greet = () => {
  toast.add({severity:"success", summary: "PrimeVue", detail: text.value})
}
</script>

<template>
  <div class="grid grid-nogutter surface-section text-800">
    <div class="col-12 md:col-6 p-6 text-center md:text-left flex align-items-center ">
        <section>
            <span class="block text-6xl font-bold mb-1">Text here</span>
            <div class="text-6xl text-primary font-bold mb-3">More text here</div>
            <p class="mt-0 mb-4 text-700 line-height-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
            
            <Button label="Learn More" type="button" class="mr-3 p-button-raised"></Button>
            <Button label="Live Demo" type="button" class="p-button-outlined"></Button>
        </section>
    </div>
    <div class="col-12 md:col-6 overflow-hidden">
        <img src="https://upload.wikimedia.org/wikipedia/commons/e/eb/Ash_Tree_-_geograph.org.uk_-_590710.jpg" alt="Image" class="md:ml-auto block md:h-full" style="clip-path: polygon(8% 0, 100% 0%, 100% 100%, 0 100%)" />
    </div>
</div>
  <div class="container">
    <Toast></Toast>
    <span class="p-float-label p-input-filled" style="margin-right:1rem">
      <InputText id="txt" type="text" v-model="text" />
      <label for="txt">Text</label>
    </span>
    <Button label="Greet" @click="greet" icon="pi pi-user"></Button>
  </div>
</template>

<style scoped>
.container{
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
</style>
