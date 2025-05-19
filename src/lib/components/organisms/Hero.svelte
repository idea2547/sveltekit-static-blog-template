<script>
	import FeaturesIcon from '$lib/icons/features.svelte';
	import GitHubIcon from '$lib/icons/socials/github.svelte';
	import Button from '$lib/components/atoms/Button.svelte';
	import Sparkles from '../atoms/Sparkles.svelte';
</script>

<section id="hero">
	<h1 class="hello">IdeaRC🚀🌌</h1>
	<p class="intro">
		<span class="left">Otaku building,</span>
		<span class="right">seeks to discover the secrets of the universe.</span>
	</p>
	<div class="ctas">
		<!-- <Sparkles>
			<Button href="https://github.com/matfantinel/sveltekit-static-blog-template">
				<GitHubIcon slot="icon" />
				Source Code
			</Button>
		</Sparkles> -->
		<!-- <Button color="primary" href="https://histoire-sveltekit-static-blog-template.vercel.app/">
			<FeaturesIcon slot="icon" />
			Components
		</Button> -->
		<Button class="nasa-btn" color="primary" href="/blog">
			<span>Read the Blog</span>
			<span class="nasa-arrow">
				<svg
					width="22"
					height="22"
					viewBox="0 0 22 22"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
				>
					<circle cx="11" cy="11" r="11" fill="#E43D25" />
					<path
						d="M10 7L14 11L10 15"
						stroke="white"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
					/>
				</svg>
			</span>
		</Button>
	</div>
</section>

<style lang="scss">
	@import '$lib/scss/breakpoints.scss';

	#hero {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		gap: 1.5rem;
		position: relative;
		min-height: 60vh;
		padding: 80px 0 80px 2vw;

		.hello {
			text-align: left;
			font-family: var(--font--default);
			font-weight: 700;
			font-size: 3.5rem;
			font-stretch: expanded;
			color: var(--color--text);
			margin-bottom: 0.5rem;
			line-height: 1.1;
		}

		.intro {
			font-weight: 500;
			font-size: 1.4rem;
			width: min(100%, 440px);
			display: flex;
			flex-direction: column;
			color: var(--color--text);
			margin-bottom: 2rem;
			text-align: left;

			.left {
				text-align: left;
			}
			.right {
				text-align: left;
			}
		}

		.ctas {
			display: flex;
			flex-wrap: wrap;
			justify-content: flex-start;
			align-items: center;
			gap: 10px;
		}

		@include for-phone-only {
			padding: 32px 0 40px 3vw;
			.hello {
				font-size: 2.1rem;
			}
			.intro {
				font-size: 1.05rem;
			}
		}
	}

	.nasa-btn {
		display: inline-flex;
		align-items: center;
		gap: 0.6em;
		font-family: var(--font--default);
		font-weight: 800;
		font-size: 2rem;
		color: #fff;
		background: none;
		border: none;
		box-shadow: none;
		padding: 0;
		transition: color 0.2s;
		text-decoration: none;

		&:hover .nasa-arrow {
			transform: scale(1.08);
			box-shadow: 0 2px 8px rgba(228, 61, 37, 0.18);
		}
	}

	.nasa-arrow {
		display: inline-flex;
		align-items: center;
		margin-left: 0.2em;
		transition: transform 0.2s, box-shadow 0.2s;
	}
</style>
