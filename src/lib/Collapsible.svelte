<script lang="ts">
  export let isActive = true;

  const toggleIsActive = () => {
    isActive = !isActive;
  };
</script>

<div class="px-4 flex space-x-4">
  {#if isActive}
    <button on:click={toggleIsActive}> REMOVE </button>
  {:else}
    <button on:click={toggleIsActive}> ADD </button>
  {/if}
</div>

{#if isActive}
  <slot />
{/if}
