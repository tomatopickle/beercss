<template lang="pug">
#textareas
  .large-space
  h4
    span Textareas
    a.chip.circle(@click="domain.showSamples(data, '#textareas .field', null, 'https://github.com/beercss/beercss/blob/main/docs/TEXTAREA.md')")
      i code
  nav.wrap
    label.checkbox
      input(type="checkbox", checked, @click="domain.updateBorder('#textareas .field', $event)")
      span border
    label.checkbox
      input(type="checkbox", @click="domain.updateRound('#textareas .field', $event)")
      span round
    label.checkbox
      input(type="checkbox", @click="domain.updateFill('#textareas .field', $event)")
      span fill
    label.radio
      input(type="radio", name="size-textareas", @click="domain.updateSize('#textareas .field', 'small')")
      span small
    label.radio
      input(
        type="radio",
        name="size-textareas",
        checked,
        @click="domain.updateSize('#textareas .field')"
      )
      span medium
    label.radio
      input(type="radio", name="size-textareas", @click="domain.updateSize('#textareas .field', 'large')")
      span large
    label.radio
      input(type="radio", name="size-textareas", @click="domain.updateSize('#textareas .field', 'extra')")
      span extra
  .space
  .row
    .col.s12.l4
      .field.textarea.border
        textarea
    .col.s12.l4
      .field.textarea.border
        textarea
        span.helper Complementary text
    .col.s12.l4
      .field.textarea.invalid.border
        textarea
        span.error Error text
    .col.s12.l4
      .field.textarea.label.border
        textarea
        label Label
    .col.s12.l4
      .field.textarea.label.border
        textarea
        label Label
        span.helper Complementary text
    .col.s12.l4
      .field.textarea.label.invalid.border
        textarea
        label Label
        span.error Error text
    .col.s12.l4
      .field.textarea.label.prefix.border
        i search
        textarea
        label Label
    .col.s12.l4
      .field.textarea.label.suffix.border
        textarea
        label Label
        i search
    .col.s12.l4
      .field.textarea.label.prefix.suffix.border
        i search
        textarea
        label Label
        i search
    .col.s12.l4
      .field.textarea.label.prefix.border
        img.circle(:src="'/favicon.png'")
        textarea
        label Label
    .col.s12.l4
      .field.textarea.label.suffix.border
        textarea
        label Label
        img.circle(:src="'/favicon.png'")
    .col.s12.l4
      .field.textarea.label.prefix.suffix.border
        img.circle(:src="'/favicon.png'")
        textarea
        label Label
        img.circle(:src="'/favicon.png'")
    .col.s12.l4
      .field.textarea.border.prefix
        a.loader
        textarea
    .col.s12.l4
      .field.textarea.border.suffix
        textarea
        a.loader
    .col.s12.l4
      .field.textarea.border.prefix.suffix
        a.loader
        textarea
        a.loader
</template>

<script setup lang="ts">
import domain from "./domain";
import data from "./data";
</script>