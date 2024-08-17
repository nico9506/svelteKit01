<script>
	import { goto, beforeNavigate, afterNavigate } from '$app/navigation';

	const handleClick = () => {
		console.log('Placing your order');
		goto('/products', { replaceState: true });
	};

	beforeNavigate((navigation) => {
		console.log({ before: navigation });
	});
	afterNavigate((navigation) => {
		console.log({ after: navigation });
	});
</script>

<h1>Neovim (Lazyvim) + SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<a href="/blog">Blog</a>
<a href="/products">Products</a>

<button on:click={handleClick}>Place Order</button>
