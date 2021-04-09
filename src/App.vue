<template>
  <div>
    <p>{{count}}</p>
    <button @click="handleClick">add</button>
  </div>
</template>

<script>
import { reactive, toRefs } from 'vue';

export default {
  name: 'App',
  setup() {
    const state = reactive({ count: 0 });
    const handleClick = () => {
      state.count++;
    };

    return {
      ...toRefs(state),
      handleClick,
    };
  },
};
</script>