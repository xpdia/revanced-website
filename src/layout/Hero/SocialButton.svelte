<script lang="ts">
	import type { Social } from '$lib/types';
	export let social = '';
	export let data: Social[];
</script>

<a
	href={data.find((jsonSocial) => jsonSocial.name.toLowerCase() === social.toLowerCase())?.url}
	rel="noreferrer"
	target="_blank"
>
	<div>
		<img src="socials/{social}.svg" alt={social} />
	</div>
</a>

<style>
	div {
		border: 0;
		width: 60px;
		height: 60px;
		padding: 14px;
		cursor: pointer;
		border-radius: 200px;
		transition: transform 0.4s var(--bezier-one);
		background-color: var(--grey-two);
		color: var(--white);
		user-select: none;
	}

	div {
		display: flex;
		justify-content: center;
	}

	img {
		transition: filter 0.4s var(--bezier-one);
		width: 30px;
	}

	div:hover {
		transform: translateY(-5%);
	}

	div:hover img {
		filter: brightness(1.2);
	}
</style>
