<script setup lang="ts">
  import { RouterView } from 'vue-router';
  import Toast from 'primevue/toast';
  import { onMounted } from 'vue';
  import { useThemeStore } from '@/utils/themeStore';

  const themeStore = useThemeStore();

  onMounted(() => {
    themeStore.initializeTheme();
  });
</script>

<template>
  <Toast />
  <!-- <transition name="fade" mode="out-in"> -->
  <RouterView />
  <!-- </transition> -->
</template>

<style scoped>
  /* Navigation styles */
  nav ul {
    list-style: none;
    padding: 0;
  }

  nav li {
    display: inline;
    margin-right: 1em;
  }
</style>

<style>
  /* Transition styles */
  .fade-enter-from {
    opacity: 0;
  }

  .fade-enter-active {
    opacity: 0;
    animation: movingIn 0.3s;
  }

  .fade-leave-active {
    animation: movingOut 0s;
  }

  @keyframes movingIn {
    0% {
      opacity: 0;
    }

    100% {
      opacity: 1;
    }
  }

  @keyframes movingOut {
    0% {
      opacity: 1;
    }

    100% {
      opacity: 0;
    }
  }
</style>

<!-- Global styles for PrimeVue -->
<style>
  .p-toast {
    width: fit-content !important;
  }
  .p-toast-message {
    border: 1px solid rgb(0, 0, 0) !important;
    border-radius: 10px !important;
  }

  .p-toast-message.p-toast-message-success {
    background-color: rgb(35, 35, 40) !important;
  }

  .p-toast-message.p-toast-message-error {
    background-color: rgb(129, 0, 0) !important;
  }

  .p-toast-message-content {
    display: flex !important;
    justify-content: start !important;
    align-items: center !important;
    padding-left: 20px !important;
    padding-right: 20px !important;
    padding-bottom: 8px !important;
    padding-top: 8px !important;
  }

  .p-toast-message-text {
    display: flex !important;
    justify-content: center !important;
    align-items: start !important;
    gap: 0px !important;
  }

  .p-toast-message-content .p-toast-summary,
  .p-toast-message-content .p-toast-detail {
    color: rgb(225, 225, 225) !important;
    font-size: 14px;
    font-weight: 500;
  }

  .p-toast-message-content svg {
    height: 18px !important;
    width: 18px !important;
    stroke: white;
    stroke-width: 1.2px;
  }

  .p-datepicker-input {
    background: white !important;
    box-shadow: none !important;
    border: 1px solid #e5e7eb !important;
    width: 160px !important;
    padding: 7px !important;
  }

  .dark .p-datepicker-input {
    background: #121212 !important;
    box-shadow: none !important;
    border: 1px solid #313131 !important;
  }

  .p-datepicker-input:focus {
    border: 1px solid #a9a9a9 !important;
  }

  .dark .p-datepicker-input:focus {
    border: 1px solid #a9a9a9 !important;
  }

  .p-datepicker-input:active {
    border: 1px solid black !important;
  }

  .p-datepicker-dropdown {
    background: white !important;
    border-right: 1px solid #e5e7eb !important;
    border-bottom: 1px solid #e5e7eb !important;
    border-top: 1px solid #e5e7eb !important;
  }

  .dark .p-datepicker-dropdown {
    background: white !important;
    border-right: 1px solid #313131 !important;
    border-bottom: 1px solid #313131 !important;
    border-top: 1px solid #313131 !important;
  }

  .dark .p-datepicker-dropdown {
    background: #121212 !important;
  }

  .p-datepicker-dropdown:hover {
    background-color: rgb(170, 170, 170) !important;
  }

  .dark .p-datepicker-dropdown:hover {
    background-color: rgb(64, 64, 64) !important;
  }

  .p-datepicker-panel {
    background-color: white !important;
  }

  .dark .p-datepicker-panel {
    background-color: #121212 !important;
  }

  .p-datepicker-panel span {
    color: black !important;
  }

  .dark .p-datepicker-panel span {
    color: #d9d9d9 !important;
  }

  .p-datepicker-header {
    background-color: white !important;
  }

  .dark .p-datepicker-header {
    background-color: #121212 !important;
  }

  .p-datepicker-header button {
    color: black !important;
  }

  .dark .p-datepicker-header button {
    color: #d9d9d9 !important;
  }

  .p-inputtext {
    color: black !important;
    font-size: 14px !important;
  }

  .dark .p-inputtext {
    color: #d9d9d9 !important;
  }

  .dark .p-datepicker-day-selected {
    background-color: green !important;
  }

  .p-select {
    background-color: white !important;
    border: 1px solid black !important;
  }

  .dark .p-select {
    background-color: #121212 !important;
    border: 1px solid #d9d9d9 !important;
  }

  .p-select-label {
    color: black !important;
  }

  .dark .p-select-label {
    color: #d9d9d9 !important;
  }

  .p-select-overlay {
    background: white !important;
  }

  .dark .p-select-overlay {
    background: #121212 !important;
  }

  .p-select-option:hover {
    background: rgb(170, 170, 170) !important;
  }

  #tiktokMusicConsent {
    background-color: white !important;
    background: white !important;
    border: 1px solid black !important;
  }

  textarea {
    outline: none; /* Prevent default outline */
    border: none; /* Initial border */
    transition: border-color 0.3s ease; /* Smooth transition for any changes */
  }

  textarea:focus,
  textarea:active {
    outline: none; /* Prevent default outline */
    border: none; /* Ensure consistent border styling */
  }
</style>
