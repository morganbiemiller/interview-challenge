<template>
  <div id="app" class="app-wrapper">
    <div class="content-wrapper">
      <div class="nav">
        <img class="nav__logo" src="./assets/logo.svg">
        <div class="nav__menu">
          <a>About</a>
          <a>Services</a>
          <a>Contact</a>
          <button class="login-button">Login</button>
        </div>
      </div>

      <div class="section section--jumbo">
        <h1>Discover & share the best content on the web</h1>
        <div class="form">
          <input type="email" placeholder="Email Address">
          <input type="password" placeholder="Password">

          <div class="checkbox">
            <label class="checkbox__label"></label>
            <input type="checkbox">
          </div>

          <button class="register-button">Register Now</button>
        </div>
      </div>

      <div class="section section--steps">
        <div class="step">
          <img src="./assets/step-1.svg">
          <h3>Watch your favorite videos all from one place</h3>
          <p>Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar.</p>
        </div>

        <div class="step">
          <img src="./assets/step-2.svg">
          <h3>Upvote your favorites to save them for later</h3>
          <p>Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar.</p>
        </div>

        <div class="step">
          <img src="./assets/step-3.svg">
          <h3>Share the best moments with your best friends</h3>
          <p>Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar.</p>
        </div>
      </div>

      <div class="section section--live">
        <div class="callout">
          <span>“My friends and I are obsessed with this app. We send funny vids to each other all day long!” - DotaStream3r86</span>
        </div>
        <div class="video-wrapper">
          <iframe src="" width="100%" height="auto"></iframe>
        </div>
      </div>

      <div class="section section--press">
        <h2>In The Press</h2>

        <div class="press-items">
          <div class="press-item">
            <div class="press-item__header">
              <img src="./assets/tc.svg">
            </div>
            <div class="press-item__content">
              <h3>Techcrunch</h3>
              <p>Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar.</p>
              <a>Read more</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>

<style lang="less">
@purple-base: #330a8b;
@purple-light: #4104c2;
@purple-dark: #1f0062;
@pink: #dc2064;
@white: #ffffff;
@grey-light: #e5e5e5;

@input: #828f92;

@padding: 16px;
@margin: 16px;

.padding {
  padding: 16px;
}

.radius {
  border-radius: 8px;
}

body {
  margin: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  font-family: "Poppins", sans-serif;
  font-size: 14px;
  background-color: @purple-base;
  color: @white;
}

* {
  box-sizing: border-box;
}

h1,
h2 {
  margin-top: 0;
}

h1 {
  font-size: 70px;
  font-weight: 700;
  margin-bottom: 0;
}

h2 {
  font-size: 24px;
  font-weight: 500;
}

h3 {
  font-size: 20px;
  font-weight: 500;
  margin: 0 0 8px 0;
}

p {
  color: @grey-light;
  margin: 0;
  line-height: 130%;
}

a {
  text-decoration: underline;
}

input {
  border: 1px solid @input;
  border-radius: 8px;
  height: 56px;
  width: 100%;
  padding: 0 @padding 0 @padding;
  background-color: transparent;
  margin-bottom: @margin;
  .radius();
}

img {
  width: 100%;
  height: auto;
}

button {
  border: 0;
  color: @white;
  padding: 0 @padding 0 @padding;
  font-weight: 500;
  font-family: "Poppins", sans-serif;
}

.app-wrapper {
  padding: 32px;
  overflow-y: auto;
  height: 100vh;
}

.content-wrapper {
  max-width: 1280px;
  margin: 0 auto;
}

.nav {
  display: grid;
  grid-template-columns: 60px 1fr;
}

.nav__menu {
  align-self: center;
  justify-self: end;
}

.login-button {
  line-height: 40px;
  background-color: @purple-dark;
  .radius();
}

.register-button {
  background-color: @pink;
  line-height: 64px;
  font-size: 16px;
  border-radius: 100px;
  width: 100%;
}

.section {
  margin-bottom: 80px;
}

.section--steps {
  display: grid;
  grid-template-rows: repeat(3, 1fr);
  grid-gap: 24px;
}

.step {
  background-color: @purple-light;
  .radius();
  .padding();
  display: grid;
  grid-template-columns: 90px 1fr;
  grid-template-rows: auto auto;
  grid-column-gap: 24px;

  img {
    grid-row: 1 / span 2;
    grid-column: 1 / span 1;
  }

  h3 {
    grid-row: 1 / span 1;
    grid-column: 2 / span 1;
  }

  p {
    grid-row: 2 / span 1;
    grid-column: 2 / span 1;
  }
}

.press-items {
  display: grid;
  grid-gap: 32px;

  @media (min-width: 800px) {
    grid-template-columns: repeat(3, 1fr);
  }
}

.press-item {
  .radius();
  overflow: hidden;
  background-color: @purple-light;
}

.press-item__header {
  height: 80px;
  background-color: @white;
  display: flex;
  align-items: center;
  justify-content: center;

  img {
    object-fit: contain;
  }
}

.press-item__body {
}
</style>
