<script lang="ts">
    import InactionCard from "../components/InactionCard.svelte";
    import type { Inaction } from "../types/Inaction";

    let inactions: Inaction = [
      {
        title: "Return VHS to Blockbuster",
        notes: "You've had it since 1998. What's the rush?",
      },
      {
        title: "Fix the hole in the wall",
        notes: "Keeping it where it is adds character and nostalgia.",
      },
      {
        title: "Do the dishes",
        notes:
          "Someone else will probably get to them. Just leave them in the sink.",
      },
    ];
  </script>

<main>
    <h1>To Don't List</h1>
    <p class="intro">Here is a list of things I'm not going to do:</p>
  
    {#each inactions as inaction}
      <InactionCard
        title={inaction.title}
        notes={inaction.notes}
      />
    {/each}
  </main>

  <style>
    main {
      max-width: 24rem;
      margin: 0 auto;
      padding: 0 1rem;
    }
    @media (min-width: 26rem) {
      main {
        padding: 0;
      }
    }
    .intro {
      color: var(--color-gray-500);
    }
  </style>