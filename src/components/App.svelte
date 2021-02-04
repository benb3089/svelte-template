<script>
  const name = 'World';
</script>

<main>
  <h1>Hello {name}!</h1>
  <h2>Heading Level 2</h2>
  <h3>Heading Level 3</h3>
  <h4>Heading Level 4</h4>
  <h5>Heading Level 5</h5>
  <h6>Heading Level 6</h6>
</main>

<style lang="scss">
  @use '../styles/app';

  @include app.reset;

  @include app.root {
    main {
      text-align: center;
      padding: 1rem;
      max-width: 240px;
      margin: 0 auto;

      @include app.screen-sm {
        max-width: none;
      }
    }

    h1 {
      color: app.$colors-blue-400;
      text-transform: uppercase;
      font-size: 3.75rem;
      line-height: 1;
    }
  }
</style>
