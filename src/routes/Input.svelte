<script>
let brand;
let model = '';
let seller = '';
let price = '';

let display = false;

function displayValues() {
    display = true;
}
</script>

<input type="text" id="brand" bind:value={brand} placeholder="brand"/>
<input type="text" id="model" bind:value={model} placeholder="model"/>
<input type="text" id="seller" bind:value={seller} placeholder="seller"/>
<input type="number" id="price" bind:value={price} placeholder="price"/>

{#if brand && model && seller && price}
<button id="add" on:click={() => displayValues()}>Add</button>
{/if}

<hr>

{#if display}
    {brand} {model} {seller} {price}
{/if}
