<template>
  <div class="container">
    <div>
      <h1 class="title">
        {{ text }}
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $microcms }) {
    const data = await $microcms.get({
      endpoint: 'hello',
    });
    return data;
  }
}
</script>
