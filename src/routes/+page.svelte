<script lang="ts">
    import type { PageData } from "./$types";
import { generations } from "./generations";



 export let data: PageData;
</script>

{#each data.monsters as monster (monster.url)}
    <h1>{monster.name}</h1>
{/each}

{#each generations as generation (generation.id)}
<h1>{generation.name}</h1>
<p>Games: {generation.games.join(', ')}</p>
<p>Main region: {generation.main_region}</p>
{/each}
<style></style>