<template>
  <nav class="navbar">
    <ul class="nav">
      <li>
        Articles
        <ul class="dropdown">
          <li>
            <a
              target="_blank"
              href="http://slovesnov.users.sourceforge.net/bullscows/bullscows.pdf"
            >
              Article in english version 3.1
            </a>
          </li>
          <li>
            <a
              target="_blank"
              href="http://slovesnov.users.sourceforge.net/bullscows/bullscows3.0.pdf"
            >
              Article in english version 3.0
            </a>
          </li>
          <li>
            <a
              target="_blank"
              href="http://slovesnov.users.sourceforge.net/bullscows/bullscows2.1.pdf"
            >
              Article in english version 2.1
            </a>
          </li>
          <li>
            <a
              target="_blank"
              href="http://slovesnov.users.sourceforge.net/bullscows/bullscows_ru.pdf"
            >
              Article in russian
            </a>
          </li>
          <li>
            <a
              target="_blank"
              href="http://slovesnov.users.sourceforge.net/bullscows/bulls_and_cows.pdf"
            >
              Article of John Francis
            </a>
          </li>
        </ul>
      </li>
      <li>
        <router-link to="/">
          Home
        </router-link> 
      </li>		
      <li>
        <router-link to="/bullscows">
          Play Bulls &amp; Cows
        </router-link>			
      </li>
      <li>
        <router-link to="/statistic">
          Statistic
        </router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
    name: 'Menu',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
html {
  height: 100%;
}

body {
  display: flex;
  flex-direction: column;
  height: 100%;
  background: #F3F4F8;
}

ul.nav {
  display: flex;
  position: relative;
  flex-direction: row;
  align-items: center;
  max-width: 0%;
  margin: 0 auto;
  padding: 0;
  list-style: none;
  background: #5BC9CA;
  border-top-left-radius: 6px;
  border-top-right-radius: 6px;
}
ul.nav > li {
  position: relative;
  flex-grow: 1;
  flex-shrink: 0;
  height: 60px;
  font-size: 11px;
  text-align: center;
  text-transform: uppercase;
  line-height: 60px;
  letter-spacing: 1px;
  color: #e7e6f1;
  cursor: pointer;
}
ul.nav > li:hover {
  background: rgba(0, 0, 0, 0.1);
}
ul.nav > li:hover ul.dropdown {
  visibility: visible;
  -webkit-transform: translate(0, 0);
          transform: translate(0, 0);
  opacity: 1;
  z-index: 0;
}
ul.nav > li:hover ul.dropdown > li {
  -webkit-animation-name: slideInLeft;
          animation-name: slideInLeft;
  -webkit-animation-duration: 0.3s;
          animation-duration: 0.3s;
  -webkit-animation-timing-function: ease-in-out;
          animation-timing-function: ease-in-out;
  -webkit-animation-fill-mode: backwards;
          animation-fill-mode: backwards;
}
ul.nav > li:first-child {
  border-top-left-radius: 6px;
}
ul.nav > li:last-child {
  border-top-right-radius: 6px;
}

ul.dropdown {
  visibility: hidden;
  display: flex;
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  flex-direction: column;
  margin: 0;
  padding: 5px 0 30px;
  list-style: none;
  color: #333;
  background: #e5e4ea;
  border-bottom-left-radius: 6px;
  border-bottom-right-radius: 6px;
  box-shadow: 1px 2px 5px -1px rgba(0, 0, 0, 0.15), 0px 4px 14px -1px rgba(0, 0, 0, 0.1);
  -webkit-transform: translate(0, -60px);
          transform: translate(0, -60px);
  transition: opacity 0.2s, z-index 0s 0.2s, -webkit-transform 0.2s ease-out;
  transition: transform 0.2s ease-out, opacity 0.2s, z-index 0s 0.2s;
  transition: transform 0.2s ease-out, opacity 0.2s, z-index 0s 0.2s, -webkit-transform 0.2s ease-out;
  opacity: 0;
  z-index: -1;
}
ul.dropdown > li {
  font-size: 11px;
  cursor: pointer;
}
ul.dropdown > li:hover {
  background: rgba(0, 0, 0, 0.06);
}

@-webkit-keyframes slideInLeft {
  from {
    -webkit-transform: translate(-25%, 0);
            transform: translate(-25%, 0);
    opacity: 0;
  }
  to {
    -webkit-transform: translate(0, 0);
            transform: translate(0, 0);
    opacity: 1;
  }
}

@keyframes slideInLeft {
  from {
    -webkit-transform: translate(-25%, 0);
            transform: translate(-25%, 0);
    opacity: 0;
  }
  to {
    -webkit-transform: translate(0, 0);
            transform: translate(0, 0);
    opacity: 1;
  }
}

</style>