<template>
  <div class="el-card" :class="shadow ? 'is-' + shadow + '-shadow' : 'is-always-shadow'">
    <div class="el-card__header" v-if="$slots.header || header">
      <slot name="header">{{ header }}</slot>
    </div>
    <div class="el-card__body" :style="bodyStyle">
      <slot></slot>
    </div>
    <div class="el-card__footer" v-if="$slots.footer || footer">
      <slot name="footer">{{ footer }}</slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ElCard',
    props: {
      header: {},
      footer: {},
      bodyStyle: {},
      shadow: {
        type: String
      }
    }
  };
</script>
