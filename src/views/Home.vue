<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <div>{{ count }}</div>
    <div>name: {{ state.name }}</div>
    <div>age: {{ state.age }}</div>
  </div>
</template>

<script>
// @ is an alias to /src
import { reactive, ref, onMounted } from 'vue';

export default {
  name: 'Home',
  setup() {
    const count = ref(0);
    const state = reactive({
      name: 'flitrue',
      age: 28,
      job: 'front coder',
    });

    onMounted(() => {
      console.log('api-url', process.env.VUE_APP_URL);
    });

    return {
      count,
      state,
    };
  },
};
</script>
