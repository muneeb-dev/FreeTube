<template>
  <div
    class="switch-ctn"
    :class="{compact}"
  >
    <input
      :id="id"
      v-model="currentValue"
      type="checkbox"
      name="set-name"
      class="switch-input"
      :checked="currentValue"
      :disabled="disabled"
      @change="$emit('change', currentValue)"
    >
    <label
      :for="id"
      class="switch-label"
    >
      {{ label }}
      <ft-tooltip
        v-if="tooltip !== ''"
        class="selectTooltip"
        :tooltip="tooltip"
      />
    </label>
  </div>
</template>

<script src="./ft-toggle-switch.js" />
<style scoped lang="sass" src="./ft-toggle-switch.sass" />
