<template>
  <div class="column content-box">
    <woot-button
      color-scheme="success"
      class-names="button--fixed-right-top"
      icon="ion-android-add-circle"
      @click="openAddPopup()"
    >
      {{ $t('ATTRIBUTES_MGMT.HEADER_BTN_TXT') }}
    </woot-button>
    <woot-modal :show.sync="showAddPopup" :on-close="hideAddPopup">
      <add-attribute :on-close="hideAddPopup" />
    </woot-modal>
  </div>
</template>

<script>
import AddAttribute from './AddAttribute';
export default {
  components: {
    AddAttribute,
  },
  data() {
    return {
      showAddPopup: false,
    };
  },
  methods: {
    openAddPopup() {
      this.showAddPopup = true;
    },
    hideAddPopup() {
      this.showAddPopup = false;
    },
  },
};
</script>

<style></style>
