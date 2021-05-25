<script>
  import { makeTitle } from '../scripts/make_title.svelte';
  import FooterInfo from '../components/footerInfo.svelte';

  export let allContent;
</script>

<footer class="isFlex">
  <div>
    <span>All content:</span>
    {#each allContent as content}
      <a href="{content.path}">{makeTitle(content.filename)}</a>
    {/each}
  </div>
  <hr class="sep">
  <FooterInfo />
</footer>

<style>
  footer {
    height: 100%;
    display: flex;
    flex-direction: column;
    /*align-items: center;*/
    /*background-color: var(--base-dark);*/
    /*margin-top: 100px;*/
    padding-top:  1rem;
    flex-shrink: 0;
  }
  span {
    color: var(--primary);
    font-weight: bold;
  }
  a {
    /*color: white;*/
    color: darkgrey;
    text-decoration: none;
    margin-left: 10px;
  }

  a:hover {
    color: tomato;
  }

  .sep {
  }
</style>
