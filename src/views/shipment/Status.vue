<template>
  <img class="small" v-if="rowData.status === 0" src="../../assets/icons/shipment_underway.svg" :alt="$t('status_transit')">
  <img class="small" v-else-if="rowData.status === 1 || rowData.status === 3" src="../../assets/icons/inside_specifications.svg" :alt="$t('status_ok')">
  <img class="small" v-else src="../../assets/icons/outside_specifications.svg" :alt="$t('status_bad')">
</template>

<script>
export default {
  props: {
    rowData: {
      type: Object,
      required: true
    },
    rowIndex: {
      type: Number
    }
  }
}
</script>

<style lang="scss" scoped>
  .small {
    height: 26px;
    vertical-align: middle;
  }
</style>
