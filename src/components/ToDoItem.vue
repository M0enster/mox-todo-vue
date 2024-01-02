<template lang="">
  <div>
    <input type="checkbox" id="todo-item" :checked="isDone" />
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
import uniqueId from "lodash/uniqueId";
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    done: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      isDone: this.done,
      id: uniqueId("todo-"),
    };
  },
};
</script>

<style></style>
