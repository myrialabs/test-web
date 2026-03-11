<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<meta name="robots" content="noindex, nofollow" />
	<link rel="icon" href={favicon} />
	<style>
		:global(body) {
			font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
			margin: 0;
			background: #f5f5f5;
		}
	</style>
</svelte:head>

<nav style="background: #333; padding: 1rem; margin-bottom: 2rem;">
	<ul style="list-style: none; margin: 0; padding: 0; display: flex; gap: 2rem;">
		<li><a href="/" style="color: white; text-decoration: none;">Home</a></li>
		<li><a href="/about" style="color: white; text-decoration: none;">About</a></li>
		<li><a href="/blog" style="color: white; text-decoration: none;">Blog</a></li>
		<li><a href="/contact" style="color: white; text-decoration: none;">Contact</a></li>
	</ul>
</nav>

<main style="max-width: 1200px; margin: 0 auto; padding: 2rem;">
	{@render children()}
</main>
