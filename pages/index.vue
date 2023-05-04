<template>
  <div class="all">
    <div class="header">
      <a href="#" class="logo"> <i class="bx bxs-movie"></i> Movies </a>
      <div class="bx bx-menu" id="menu-icon"></div>
      <ul class="navbar">
        <li><a href="#home" class="home-active">Home</a></li>
        <li><a href="#movies">Movies</a></li>
        <li><a href="#coming">Coming</a></li>
        <li><a href="#newsletter">Newsletter</a></li>
      </ul>
      <a href="#" class="btn"> Sign In </a>
    </div>
    <div>
      <section class="home swiper" id="home">
        <div class="swiper-wrapper">
          <div class="swiper-slide container">
            <img src="../assets/imgs/your_name.jpg" alt="" />
            <div class="home-text">
              <h1> Your Name </h1>
              <span>What is your name ?</span>
              <a href="#" class="btn"> Watch now </a>
              <a href="#" class="play">
                <i class="bx bx-play"></i>
              </a>
            </div>
          </div>
        </div>
        <div class="swiper-pagination"></div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  head: {
    script: [
      {
        src:"https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.js",
        section: true,
      },
    ],
  },
  methods: {
    slide() {
      var swiper = new Swiper(".home", {
      spaceBetween: 30,
      centeredSlides: true,
      autoplay: {
        delay: 2500,
        disableOnInteraction: false,
      },
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
      },
    });
    },
  },
};
</script>

<style lang="scss" scoped>

@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,600;1,600&display=swap");
* {
  font-family: "Poppins", sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
  scroll-padding-top: 2rem;
  scroll-behavior: smooth;
}
.header {
  position: fixed;
  width: 100%;
  top: 0;
  right: 0;
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 100px;
  transition: 0.5s;
  background: #ff2c1f;
}
.logo {
  font-size: 1.1rem;
  font-weight: 600;
  color: #fff;
  display: flex;
  align-items: center;
  column-gap: 0.5rem;
}
.logo .bx {
  font-size: 24px;
  color: #fff;
}
.navbar {
  display: flex;
  column-gap: 5rem;
}
.navbar li {
  position: relative;
}
.navbar a {
  font-size: 1rem;
  font-weight: 500;
  color: #fff;
}
.navbar a::after {
  content: "";
  width: 0;
  height: 2px;
  background: #141212;
  position: absolute;
  bottom: -4px;
  left: 0;
  transition: 0.4s all linear;
}
.navbar a:hover::after,
.navbar .home-active::after {
  width: 100%;
}
#menu-icon {
  font-size: 24px;
  cursor: pointer;
  z-index: 1000001;
  display: none;
}
.btn {
  padding: 0.7rem;
  background: #fff;
  color: #141212;
  font-weight: 400;
  border-radius: 0.5rem;
}
.btn:hover {
  background: #a4d646;
}
section {
  padding: 4.5rem 0 1.5rem;
}
.container{
  width: 100%;
  margin: auto;
  min-height: 640px;
  position: relative;
  display: flex;
  align-items: center;
  background: rgb(2,3,7,0.4);
}
.container img{
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  z-index: -1;
}
.swiper-pagination-bullet{
  width: 6px !important;
  height: 6px !important;
  border-radius: 0.2rem !important;
  background: #fff !important;
  opacity: 1 !important;
}
.swiper-pagination-bullet-active{
  width: 1.5rem !important;
  background: #ff2c1f !important;
}
.home-text{
  z-index: 1000;
  padding: 0 150px;
}
.home-text span {
  color: #fff;
  font-weight: 500;
  text-transform: uppercase;
}
.home-text h1{
  color: #fff;
  font-size: 4rem;
  font-weight: 700;
  margin-bottom: 1rem;
}
</style>
