<script lang="ts">
  import { getDrawerStore } from '@skeletonlabs/skeleton';

  interface Props {
    menuButton?: boolean;
  }

  let { menuButton = true }: Props = $props();

  const drawerStore = getDrawerStore();
  function toggle() {
    $drawerStore.open = !$drawerStore.open;
  }
</script>

<div class="flex items-center gap-8">
  {#if menuButton}
    <button type="button" aria-label="Toggle menu" onclick={toggle}>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="h-6 w-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
        />
      </svg>
    </button>
  {/if}

  <a href="/">
    <img src="/logos/svelte-maplibre-logo-monochrome-dark.svg" alt="Svelte Maplibre" class="h-10" />
  </a>
</div>
