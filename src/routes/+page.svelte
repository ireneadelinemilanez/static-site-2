<!--
  This is you page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import ImageWithCaption from '$lib/components/ImageWithCaption.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'How one Southern California-based cannabis company made an award-winning edible';
  let byline = 'Irene Adeline Milanez';
  let pubDate = '2025-07-29';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
  ];
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | NYCity News Service</title>
  <meta name="description" content="At the Craig Newmark Graduate School of Journalism at the City University of New York, change is in our DNA. That comes of being born in 2006, as the digital revolution was transforming our profession in ways none of us could have imagined." />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: CUNY Journalism School building -->
  <ImageWithCaption
    src="/cannabis.webp"
    alt="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    caption="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    credit="Craig Newmark Graduate School of Journalism"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      Edibles are often flavored to mask the taste of cannabis, but a Southern California-based company won gold by doing the opposite.
    </p>

    <p>
      Earlier this month, cannabis industry leaders took home more than 150 medals and the prestigious Golden Bear awards in nine categories, including pre-rolls, beverages, wellness products and edibles, at the California State Fair.
    </p>

    <p>
      The cannabis competition was added to the fairgrounds in 2022, joining traditional agricultural industries like craft wines and cheeses. More than 600 entries in the competition were judged on a 100-point rating system assessing aroma, flavor, appearance and experience.
    </p>

    <p>
      Among the top honors in the edibles category were Kiva Lost Farm’s Strawberry × Pink Jesus Live Resin Chews (bronze), Spinello’s Prickly Pear Liquid Diamond Infused Fruit Chews (silver) and Ay Papi’s Whitethorn Rose Single Origin Live Rosin Infused Gummies, which won both the gold medal and the Golden Bear.
    </p>

    <p>
      “There are a lot of variables that go into making an award-winning product, and it starts with the genetics and the craft farms,” Justin Lee, founder of La Habra- based Ay Papi, said.
    </p>

  </ArticleBody>

  <!-- Related Stories: Links to other articles -->
  <RelatedLinks
    title="Related Stories"
    links={relatedStories}
  />

</div>

<style>
  /* Styles here only apply to this page */
  .container {
    padding: var(--spacing-lg) var(--spacing-md);
  }
</style>