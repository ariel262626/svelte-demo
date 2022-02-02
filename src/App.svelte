<script>
	export let name;

	let rand = 0

	$: reactive = rand * 2

	function setRand() {
		rand = Math.random()
	}
</script>
<body>
	<main>
		<h1 class="title">Hello {name}!</h1>
		<p>Random number is: {rand}</p>
		<p>Random number 2X is: {reactive}</p>

		<div><button on:click={setRand}>Shuffle</button></div>
		<input bind:value={name}/>
	</main>
</body>

<style>
	body {
		width: 100%;
		height: 100%;
		background: rgba(16, 34, 52, 0.8);
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ffb4be;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	p {
		color: wheat;
	}

	button {
		color: #333333;
		background-color: #FFC0C7;
		margin: 1rem 0
	}

	.title {
		font-size: 4rem;
		font-weight: 400;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
