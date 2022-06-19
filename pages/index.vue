<template>
  <div class="home container">
    <div class="home-title">
      <h2>
        <span>Hey</span>
        <div class="hand">
          <img src="~/static/91598-hi-hand.gif" alt="">
        </div>
      </h2>
    </div>
    <div class="home-name">
      <h1>My name is Ali</h1>
    </div>
    <div class="home-description">
      <p>
        I'm a professional front end developer with over 5 years experience.
        Working on a wide range of small, medium and large-scale projects. <br>
        I am the creator of the <strong>Arabic Slug Library</strong> works
        with
        <a target="_blank" href="https://www.npmjs.com/package/arabic-slug">
          <span>JavaScript Frameworks</span>
        </a>
        and <a target="_blank" href="https://packagist.org/packages/alik/araslug"><span>Laravel</span></a>
      </p>
      <p>You can follow me on <a target="_blank" href="https://twitter.com/itsAliKhalouf"><span>Twitter</span></a>, <a
          target="_blank" href="https://www.linkedin.com/in/khaloufali/"><span>Linkedin</span></a> and <a
          target="_blank" href="https://github.com/itsalimanuel"><span>Github</span></a>. <br>
        you can check my aniamtion on <a target="_blank" href="https://codepen.io/itsalimanuel"><span>codepen</span></a>
      </p>
      <p>Contact me: <a href="mainto:itskhaloufali@gmail.com"><span>itskhaloufali@gmail.com</span></a></p>
    </div>
    <div class="home-cases">
      <a target="_blank" href="https://www.carbonmobile.com/"><span>Carbon</span></a>
      <a target="_blank" href="https://media-ppl.ru/"><span>PPL</span></a>
      <a target="_blank" href="https://choose.digital/"><span>Choose</span></a>
      <a target="_blank" href="http://saghiry.com/"><span>Saghiry</span></a>
      <a target="_blank" href="https://ferrumpanel.ru"><span>Ferrum</span></a>
      <a target="_blank" href="https://glav-pitomnik.ru/"><span>Pitomnik</span></a>
      <a target="_blank" href="https://rubin.pro/"><span>Rubin</span></a>
      <a target="_blank" href="https://дымнадом.рф"><span>дымнадом</span></a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.home {
  position: relative;

  &-title {

    h2 {
      display: flex;
      align-items: center;

      span {
        font-size: 2.5em;
        font-weight: 500;
        margin-bottom: 0;
      }

      img {
        margin-left: 20px;
        width: 2.5em;
        height: 2.5em;
      }
    }
  }

  &-name {
    margin-top: 30px;

    h1 {
      font-size: 30px;
      color: #121314;
    }
  }

  &-description {

    p {
      margin-top: 30px;
      font-size: 1.6em;
      font-weight: 400;
      line-height: 1.4;
      max-width: 28em;

      a {
        position: relative;
        z-index: 5;
        text-decoration: none;
        color: #121314;

        span {
          position: relative;
          z-index: 3;
        }

        &:hover {
          &::before {
            height: 100%;
          }
        }

        &::before {
          content: "";
          position: absolute;
          width: 100%;
          transition: .2s all;
          bottom: 0;
          left: 0;
          z-index: 1;
          height: 15px;
          background-color: #F5E73E;
        }
      }
    }
  }

  &-cases {
    display: grid;
    margin-top: 40px;
    max-width: 500px;
    grid-template-columns: repeat(4, 1fr);

    @media screen and (max-width: 768px) {
      grid-template-columns: repeat(2, 1fr);
    }

    a {
      // border-style: ;
      border: dashed #121314;
      padding: 20px;
      text-decoration: none;
      color: #121314;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;

      &:hover {
        &::before {
          height: 100%;
        }

        font-weight: bold;
      }

      &::before {
        content: "";
        position: absolute;
        width: 100%;
        transition: .2s all;
        bottom: 0;
        left: 0;
        z-index: 1;
        height: 0px;
        background-color: #F5E73E;
      }

      span {
        font-size: 1rem;
        position: relative;
        z-index: 2;
      }
    }
  }
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>

<script>


export default {
  name: 'IndexPage',
  data() {
    return {
      title: 'Ali Khalouf'
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Front end developer with over 5 years experience. wokring with React,Vue,Vite,Nuxt and Next JS Libs!'
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: 'frontend,frone-end,scss,sass,reactjs,react,next,nextjs,vue,vuejs,vite,vitejs,nuxt,nuxtjs,frameworks,aniamtion,animationjs,gsap,greensock,timeline'
        }
      ],
      link: [
        {
          rel: 'icon',
          type: 'image/x-icon',
          href: '/91598-hi-hand.gif'
        }
      ]
    }
  }
}
</script>
