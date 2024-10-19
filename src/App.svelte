<script>
  import Counter from './lib/Counter.svelte'
  import Masik from './lib/Masik.svelte'
  var selected = 'mv'
</script>

<main>
  <div class="menu">
    <button on:click={() => (selected = 'Counter')}>Counter</button>
    <button on:click={() => (selected = 'mv')}>Másik valami</button>
  </div>
  <div>
    {#if selected === 'mv'}
      <Masik />
    {:else if selected === 'Counter'}
      <Counter />
    {/if}
  </div>
</main>

<style>
  div.menu {
    position: fixed;
    top: 0px;
    left: 0px;
    width: 100%;
    height: 20px;
    background-color: #333;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  div.menu button {
    font-size: 12px;
    padding: 2px 20px;
    margin: 2px;
  }
</style>
