<script>
  const heading = "Weird";
  const subheading = `a way to <span class='italicize'>be</span> on the web`;
</script>

<div class="stars"></div>
<section class="hero">
  <div class="container">
    <div class="content">
      <div class="hero-copy">
        <h1>{heading}</h1>
        <p>{@html subheading}</p>
      </div>
      <div class="image">
        <div class="full-size">
          <img alt="keyboard and monitor" height="450" src="/hero.svg" />
        </div>
        <div class="small-size">
          <img alt="keyboard" height="300" src="/keyboard.svg" />
          <img alt="monitor" height="200" src="/Screen.svg" />
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .stars {
    background: url("/stars.avif");
    /* extend a bit more than the viewport */
    height: 175vh;
    width: 100%;
    background-position: center;
    position: absolute;
    left: 0;
    top: 0;
    z-index: -1;
  }

  .content {
    display: grid;
    place-items: center;
    margin-top: 8em;
    margin-bottom: 8em;

    .hero-copy {
      display: grid;
      place-items: center;

      h1 {
        font-family: "Rubik Mono One", monospace;
        font-weight: 400;
        font-size: 13em;
        color: #fff5bf;
        text-shadow: -9px -6px #f55134;

        /* prefix required for all browsers */
        -webkit-text-stroke-width: 2.5px;
        -webkit-text-stroke-color: black;

        @media (max-width: 1200px) {
          font-size: 13em;
        }

        @media (max-width: 800px) {
          font-size: 11em;
        }

        @media (max-width: 700px) {
          font-size: 9em;
        }
      }

      p {
        color: white;
        font-weight: 700;
        font-size: 3em;

        @media (max-width: 1200px) {
          font-size: 2.5em;
        }

        @media (max-width: 800px) {
          font-size: 2em;
        }

        @media (max-width: 700px) {
          font-size: 1.5em;
        }
      }
    }
  }

  .image {
    img {
      width: 1050px;

      @media (min-width: 1200px) {
        /* push the image up */
        margin-top: -5em;
      }

      @media (max-width: 1200px) {
        width: 750px;
      }
    }
  }

  .small-size {
    display: none;

    @media (max-width: 800px) {
      display: grid;
      grid-auto-flow: column;
      place-items: center;
      gap: 2em;
    }
  }

  @media (max-width: 800px) {
    .full-size {
      display: none;
    }

    img {
      margin-top: 8em;
      width: 100%;
    }
  }

  @media (max-width: 700px) {
    .image img {
      margin-bottom: 5em;
      width: 90%;
    }
  }
</style>
