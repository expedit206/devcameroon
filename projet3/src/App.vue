<script setup>
import { ref } from "vue";

const count = ref(0);
</script>

<template>
  <div class="app-container">
    <header class="header">
      <div class="logo">🚀 Projet 3</div>
      <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
      </nav>
    </header>

    <main class="main-content">
      <h1>Bienvenue dans ton Projet Vue 3 !</h1>
      <p class="subtitle">
        Ton application a été créée avec succès depuis le terminal.
      </p>

      <div class="card">
        <button type="button" @click="count++">
          Compteur intelligent: {{ count }}
        </button>
        <p>
          Commence par éditer <code>src/App.vue</code> pour voir tes
          changements.
        </p>
      </div>
    </main>
  </div>
</template>

<style scoped>
.app-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: #0f172a;
  color: #f8fafc;
  font-family: "Inter", system-ui, Avenir, Helvetica, Arial, sans-serif;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background: rgba(30, 41, 59, 0.7);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.logo {
  font-size: 1.5rem;
  font-weight: 700;
  background: linear-gradient(135deg, #3b82f6, #10b981);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

nav a {
  color: #cbd5e1;
  text-decoration: none;
  margin-left: 1.5rem;
  font-weight: 500;
  transition: color 0.2s;
}

nav a:hover {
  color: #3b82f6;
}

.main-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  text-align: center;
}

h1 {
  font-size: 3.5rem;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, #10b981, #3b82f6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.subtitle {
  font-size: 1.25rem;
  color: #94a3b8;
  margin-bottom: 3rem;
}

.card {
  background: rgba(30, 41, 59, 0.5);
  padding: 2.5rem;
  border-radius: 1rem;
  border: 1px solid rgba(255, 255, 255, 0.05);
  box-shadow:
    0 20px 25px -5px rgba(0, 0, 0, 0.5),
    0 8px 10px -6px rgba(0, 0, 0, 0.5);
  max-width: 500px;
  width: 100%;
}

button {
  border-radius: 0.5rem;
  border: none;
  padding: 0.8em 1.5em;
  font-size: 1.1rem;
  font-weight: 600;
  font-family: inherit;
  background: linear-gradient(135deg, #3b82f6, #2563eb);
  color: white;
  cursor: pointer;
  transition:
    transform 0.2s,
    box-shadow 0.2s;
  margin-bottom: 1.5rem;
  width: 100%;
}

button:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 15px -3px rgba(59, 130, 246, 0.5);
}

button:active {
  transform: translateY(0);
}

code {
  background: #1e293b;
  padding: 0.2rem 0.5rem;
  border-radius: 0.25rem;
  color: #38bdf8;
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
}
</style>
