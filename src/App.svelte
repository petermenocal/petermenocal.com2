<script>
  import {onMount} from 'svelte'
  onMount(()=>{
    let vh = window.innerHeight * 0.01;
    document.documentElement.style.setProperty('--vh', `${vh}px`);
    window.addEventListener('resize', () => {
      let vh = window.innerHeight * 0.01;
      document.documentElement.style.setProperty('--vh', `${vh}px`);
    });
  })
</script>

<main>
	<span id="title">peter menocal</span>
  <span>software_engineer</span>
  <span><a href='mailto:peter@geekypixel.com' title="mail">contact</a></span>
</main>

<style>
	main {
		text-align: center;
		max-width: 240px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    height: calc(var(--vh, 1vh) * 100);
		margin: 0 auto;
	}
  span {
    color: #171717;
  }

	#title {
    display: block;
		color: whitesmoke;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
