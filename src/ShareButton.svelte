<script>
  export let href;
  export let label = '';
  export let fill = true;
  export let ariaLabel = '';
  let classes = '';

  export { classes as class };
</script>

<style>
:global(.ssbc-button__link,
.ssbc-button__icon) {
  display: inline-block;
}

:global(.ssbc-button__link) {
  text-decoration: none;
  color: #fff;
}

:global(.ssbc-button) {
  transition: 25ms ease-out;
  padding: 0.75em;
}

:global(.ssbc-button__icon) :global(svg) {
  width: 1em;
  height: 1em;
  margin: 0;
  vertical-align: middle;
}

:global(.ssbc-button__icon--fill) {
  fill: #fff;
  stroke: none;
}

:global(.ssbc-button__icon--outline) {
  fill: none;
  stroke: #fff;
}
</style>

<a class="ssbc-button__link link external" {href} target="_blank" rel="noopener" aria-label={ariaLabel}>
  <div class="ssbc-button {classes}">
    <div aria-hidden="true" class="ssbc-button__icon" class:ssbc-button__icon--fill={fill} class:ssbc-button__icon--outline={!fill}>
      <slot></slot>
    </div>
    {label}
  </div>
</a>
