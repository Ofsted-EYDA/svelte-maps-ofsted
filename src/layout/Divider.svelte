<script>
	//import { themes } from '../config.js';
	import { getContext } from 'svelte';

  export let theme = getContext('theme');
  export let hr = true;
</script>

<section style="color: {themes[theme]['text']}; background-color: {themes[theme]['background']};">
	<div class="col-medium">
    {#if hr}
    <hr style="color: {themes[theme]['muted']}"/>
    {:else}
    <hr style="color: {themes[theme]['muted']}; border: none;"/>
    {/if}
	</div>
</section>

<style>
  hr {
    width: 75px;
    border: none;
    border-top: 5px solid;
    border-bottom: 5px solid;
    margin: 10px auto 80px auto;
  }
</style>

