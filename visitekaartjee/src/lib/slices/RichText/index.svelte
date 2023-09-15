	<script>
		import { PrismicRichText } from '@prismicio/svelte';
		import { PrismicImage } from '@prismicio/svelte';
		import { PrismicLink } from '@prismicio/svelte';

		/** @type {import("@prismicio/client").Content.RichTextSlice} */
		export let slice;
	</script>

	<div class="grid-container">
		<div class="grid">
			<div class="div1">
				<section class="img">
					<PrismicLink field={slice.primary.github_link}>
						<PrismicImage field={slice.primary.image} />
					</PrismicLink>
				</section>
			</div>
			<section class="name">
				<PrismicRichText field={slice.primary.content} />
			</section>
			<section class="github">
				{slice.primary.github_tag}
			</section>
		</div>
	</div>

	<style>
		@import url('https://fonts.googleapis.com/css2?family=Syncopate&display=swap');
		@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

		.grid-container {
			display: grid;
			justify-items: center;

			grid-template-columns: repeat(1, 1fr);
			grid-template-rows: 1fr 1fr;
			/* grid-column-gap: 100px; */
			grid-row-gap: 75px;
			padding-top: 100px;
			background: linear-gradient(360deg, rgb(255, 0, 0) -200%, #000000 100%);
		}

		.grid {
			display: flex;
			flex-direction: column;
			align-items: flex-start;
		}

		.name {
			color: #FB5669;
			font-family: 'Syncopate', sans-serif;
			font-size: 20px;
			font-style: normal;
			font-weight: 700;
			line-height: normal;
			letter-spacing: 0.24px;
			padding-top: 20px;
		}

		.github {
			font-family: 'Poppins', sans-serif;
			color: #FB5669;
		}

		.div1 {
			width: 300px;
			height: 300px;
			flex-shrink: 0;
			border-radius: 20px;
			background: #d9d9d9;
		}

		@media only screen and (min-width: 31em) {

		}

		@media only screen and (min-width: 45em) {
			
		}

		@media only screen and (min-width: 68em) {
			
		}
	</style>
