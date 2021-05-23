<script>
	let Casterminion = 0;
	let Meleeminion = 0;
	let Canonminion = 0;
	let items = 0; 
	
	let gold = 0;
	function CasterMinion() {
		Casterminion = Casterminion + 14;
		gold = gold + 14;
	}
	function MeleeMinion() {
		Meleeminion = Meleeminion + 21;
		gold = gold + 21;
	}
	function CanonMinion() {
		Canonminion = Canonminion + 90;
		gold = gold + 90;
	}
	

	function reset() {
		
		gold = gold - 3100;
		items = items + 1 
		Canonminion = 0 
	    Meleeminion = 0 
		Casterminion = 0 
	}
</script>

<main>
	<h1>Item shop</h1>
	<h4>One item costs 3100 gold</h4>
	<h5>Click on the minions to earn gold!
	    14 for Caster minions
		21 for Melee minions 
		90 for Cannon minions
	</h5>
	<h3>{items} Items  </h3>

	<h2>{gold} Gold </h2>

	<button on:click={CasterMinion}>Caster minion: {Casterminion} Gold</button>

	<button on:click={MeleeMinion}>Melee minion: {Meleeminion} Gold </button>



	<button on:click={CanonMinion}>Cannon minion: {Canonminion} Gold</button>
	<p></p>
	<button on:click={reset}>Buy</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		background-color: burlywood;
	}
	h1 {
		color: darkgreen;
		text-transform: uppercase;
		font-family: 'Times New Roman', Times, serif;
		font-size: 4em;
		font-weight: 100;
	}
	h2 {
		color: darkgreen;
		font-family: 'Times New Roman', Times, serif;
		font-size: 3em;
		font-weight: 100;
		background-color: burlywood;
	}
	button {
		color: purple;
		font-family: 'Arial', Times, serif;
		font-size: 2em;
		font-weight: 100;
		background-color: darkcyan;
		border: purple;
	
	}
	@media (min-width: 900px) {
		main {
			max-width: none;
		}
	}
</style>
