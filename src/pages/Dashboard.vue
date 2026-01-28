<template>
  <div class="flex">
    <div v-if="!$root.isMobile">
      <MonitorList :scrollbar="true" />
    </div>

    <div class="ml-[510px] w-full px-3">
      <!-- Add :key to disable vue router re-use the same component -->
       <div class="max-w-[1024px] mx-auto">
        <router-view :key="$route.fullPath"/>
       </div>
    </div>
  </div>
</template>

<script>
import MonitorList from "../components/MonitorList.vue";

export default {
  components: {
    MonitorList,
  },
  data() {
    return {};
  },
  mounted() {
  },
};
</script>

<style lang="scss" scoped>
</style>
