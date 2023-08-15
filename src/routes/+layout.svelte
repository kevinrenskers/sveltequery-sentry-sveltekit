<script lang="ts">
  import "../app.css";
  import { QueryClientProvider } from "@tanstack/svelte-query";
  import type { PageData } from "./$types";

  export let data: PageData;
</script>

<QueryClientProvider client={data.queryClient}>
  <div>
    <a href="/">Home</a>
    <a href="/articles">Articles</a>
  </div>
  <main>
    <slot />
  </main>
</QueryClientProvider>
