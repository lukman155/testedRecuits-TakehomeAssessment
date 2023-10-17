<script>
  let ms1 = false;
  let ms2 = false;

  let selected = false;

  const handleClick = (x) => {
    selected = x
  }

  const toggleMs1 = () => {
  ms1 = !ms1;
};

const toggleMs2 = () => {
  ms2 = !ms2;
};
</script>

<section class='hero-section' >
  <div class="hero-wrapper">
    <header>
      <a href="/"><img src="logo.png" alt="logo"></a>
      <nav>
        <a href="#history">01. HISTORY</a>
      <a href="#team">02. TEAM</a>
      </nav>
    </header>
  </div>
</section>

<div class="nav">
  <header>
    <div class="logo"><a href="/"><img src="logo.png" alt="logo"></a><p>LOSANGELES<br><span>MOUNTAINS</span></p></div>
    <nav>
      <a href="#history">01. HISTORY</a>
      <a href="#team">02. TEAM</a>
    </nav>
  </header>
</div>

<section id="history" class='history-section'>
  <div class="hero-wrapper">
    <div class="title">01.<span>HISTORY</span></div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque libero earum accusamus, provident dicta, placeat voluptatem consequatur delectus tempore beatae illo quibusdam deleniti quis ratione aliquid sint! Esse, unde non!</p>
  </div>

<div class="carousel-con">
  <div class="carousel">
    <img src="man.png" alt="man">
    <img src="mount.jpg" alt="mount">
    <img src="man.png" alt="man">
    <img src="mount.jpg" alt="mount">
  </div>
</div>

</section>

<section class='climb-section' id="team">

  <div class="hero-wrapper climb-wrapper">
    <div class="title">02.<span class="climb">CLIMB</span></div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque libero earum accusamus, provident dicta.</p>
  </div>


  <div class="tabs desktop">
    <div class="wrapper">
    <h3 on:click={() => handleClick(false)} class={selected?'':'active'}>Mountain 1</h3>
    <h3 on:click={() => handleClick(true)}  class={selected?'active':''}>Mountain 2</h3>
  </div>
  </div>

  <div class="tab-container desktop {!selected? 'tab1-img': 'tab2-img'}">
    <div class="tab-wrapper">
      {#if !selected}
      <div class="tab1">
        <h2>SCHEDULE</h2>
        <div class="item">
          <p>25 Nov 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <div class="item">
          <p>28 Nov 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>18 Dec 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>7 Jan 2017</p>
          <p>Vestibulum viverra</p>
        </div>
      </div>
  
      {/if}

      {#if selected}
      <div class="tab1">
        <h2>SCHEDULE</h2>
        <div class="item">
          <p>17 Nov 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>13 Dec 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <div class="item">
          <p>28 Dec 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>9 Feb 2017</p>
          <p>Vestibulum viverra</p>
        </div>
      </div>
      {/if}
  </div>
  </div>

<div class="accordion mobile">
  <div class="tabs">
    <div class="wrapper">
      <h3 on:click={() => toggleMs1()} class={ms1 ? 'active' : ''}>Mountain 1</h3>
    </div>
  </div>
  
  {#if ms1}
  <div class="tab-container tab1-img">
      <div class="tab-wrapper">
      <div class="tab1">
        <h2>SCHEDULE</h2>
        <div class="item">
          <p>25 Nov 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <div class="item">
          <p>28 Nov 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>18 Dec 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>7 Jan 2017</p>
          <p>Vestibulum viverra</p>
        </div>
      </div>
      </div>
    </div>
      {/if}

      <div class="tabs accord2">
        <div class="wrapper">
          <h3 on:click={() => toggleMs2()} class={ms2 ? 'active' : ''}>Mountain 2</h3>
        </div>
      </div>

      {#if ms2}
      <div class="tab-container tab2-img">
      <div class="tab-wrapper">
      <div class="tab1">
        <h2>SCHEDULE</h2>
        <div class="item">
          <p>17 Nov 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>13 Dec 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <div class="item">
          <p>28 Dec 2016</p>
          <p>Vestibulum viverra</p>
        </div>
        <br>
        <div class="item">
          <p>9 Feb 2017</p>
          <p>Vestibulum viverra</p>
        </div>
      </div>
      </div>
      </div>
      {/if}
</section>


  <footer>
    <div class="wrapper">
      <div class="logo"><a href="/"><img src="logo.png" alt="logo"></a><p>LOSANGELES<br>MOUNTAINS</p></div>
      <p>COPYRIGHT 2016. ALL RIGHTS RESERVED.</p>
    </div>
    </footer>



<style>

  .climb-wrapper p {
    margin-left: 70px;
    font-size: 14px;
  }

  footer {
    background-color: #414f6b;
    padding: .5em;
  }

  footer .wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
  }

  footer p {
    font-size: larger;
    color: #63769d;
  }

  footer img {
    opacity: .3;
  }

  .mobile {
    display: block;
  }

  .desktop {
    display: none;
  }

  .accordion {
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  .accordion h3 {
    width: 100%;
  }

  .accord2 {
    align-self: flex-end;
  }


  .tab-wrapper {
    max-width: 800px;
    width: 100%;
    margin: 0 auto;
  }

  .tab1-img {
    background-image: url(tab1.jpg);
    height: 500px;
    background-size: cover;
    background-repeat: no-repeat;  
    background-position: bottom center;
  }

  .tab2-img {
    background-image: url(tab2.jpg);
    height: 500px;
    background-size: cover;
    background-repeat: no-repeat;  
    background-position: bottom center;
  }

  .tab1 {
    margin: 5em auto;
    width: fit-content;
  }



  .tabs {
    
    width: 100%;
    background-color: #414f6b;

  }

  .tabs > div {
    display: flex;
    max-width: 900px;
    margin: 0 auto;
  }

  .tabs > div > h3 {
    padding: 10px 20px;
    cursor: pointer;
    color: rgba(255, 255, 255, 0.5);
  }

  div > h3.active {
    color: #515e71;
    background-color: rgba(255, 255, 255, 0.5);
    text-decoration: underline;
  }

  h3:hover {
    color: #515e71;
    background-color: rgba(255, 255, 255, 0.5);
    text-decoration: underline;
  }

  .tab1 {
    background-color: white;
    padding: 2em;
  }

  .item {
    display: flex;
    gap: 50px;
    justify-content: space-between;

  }

.climb-section {
    display: flex;
    flex-direction: column;
  }

  .climb-wrapper {
    display: flex;
    align-items: center;
    gap: 10px;

  }



  .climb-wrapper > p {
    line-height: 30px;
  }

  .carousel {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    height: 100%;
  }

  .carousel > img {
    max-width: 40%;
  }

  .carousel-con {
    width: 100%;
    background-color: #37435aa7;
    padding: 30px 0;

  }

  .title {
    font-size: 128px;
    margin: 0;
    position: relative;
    color: #677893;
    position: relative;
    width: fit-content;
    left: 30px;
  }

  .title > span {
    position: absolute;
    color: #414f6b;
    font-size: 24px;
    bottom: 42px;
    right: -58px;
  } 
  span.climb {
    right: -37px;

  }

.history-section {
    background-image: url(bg2.jpg);
    height: 800px;
    background-size: cover;
    background-repeat: no-repeat;  
    background-position: top center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  img {
    background-color: transparent;
  }

  .hero-section {
    background-image: url(hero.jpg);
    height: 500px;
    background-size: cover;
    background-repeat: no-repeat;  
    background-position: top center;
    
  }

  .hero-wrapper {
    padding: .5em;
    max-width: 800px;
    margin: 0 auto;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 1em;
  }

  nav {
    display: flex;
    gap: 1em;
  }

  a {
    color: white;
    text-underline-offset: 5px;
    margin: 0;
    transition: all .2s ease-out;
  }

  a:hover {
    text-underline-offset: 10px;
  }

  .nav {
    max-width: 800px;
    margin: 0 auto;
    padding: 1em 0;
  }

  .logo {
    display: flex;
    gap: 1em;
  }

  p {
    margin: 10px;
    color: #191b1ca9;
    font-size: 1em;
  }

  p > span {
    color: #414f6b;
  }


  .nav a {
    text-align: right;
    color: #414f6b;
  }

  @media (min-width: 800px){

    
  .carousel > img {
    max-width: 22%;
    padding: 2em 0;
  }

    nav {
    gap: 3em;
  }

    .hero-section {
    height: 800px;
  }

    .mobile {
      display: none;
    }
    
    .desktop {
      display: block;
    }

    .title {
    font-size: 128px;
    margin: 0;
    position: relative;
    color: #677893;
    position: relative;
    width: fit-content;
    left: -50px;
  }

  .title > span {
    position: absolute;
    color: #414f6b;
    font-size: 24px;
    bottom: 42px;
    right: -58px;
  }

  .tab1 {
    margin: 0;
    margin-top: 5em;
    width: fit-content;
  }



  }
</style>