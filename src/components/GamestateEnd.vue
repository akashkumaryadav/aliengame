<template>
  <div class="modal">
    <h1 :style="{ color: status }">
      {{ uiState }}
    </h1>
    <h1>you score is {{ score }}</h1>
    <slot></slot>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["score", "uiState"])
  },
  props: ["status"]
};
</script>
