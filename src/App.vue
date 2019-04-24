<template>
  <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <contact-list :pseudoSlot="contact => contact.name.first">
        <template v-slot="slotProps">
          {{ slotProps.customer.name.last }}
          {{ slotProps.customer.name.first }}
          <h3>{{ slotProps.date }}</h3>
        </template>
      </contact-list>
    </div>
  </div>
</template>

<script>
import ContactList from "./components/ContactList.vue";

export default {
  components: {
    ContactList
  },
  data() {
    return {};
  }
};
</script>

<style src="./assets/css/app.css"/>
