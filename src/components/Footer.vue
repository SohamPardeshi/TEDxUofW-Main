<template>
  <div class="footer">
    <div class="main-part">
    <h2 class="our-name">TEDxUofW 2021</h2>
    <h3 class="our-event-date">APRIL 17th, 2021 <br>10:00 AM to 2:00 PM PDT</h3>

    <a class="home-page-button" href="#">
      <img class="our-logo" src="/static/logo_2021.svg" alt="TEDxUofW logo"/>
    </a>
      <div class="social">
        <div class="social-bubbles">
          <a href="https://www.facebook.com/TEDxUofW/" target="_blank" class="social-bubble"><img src="/static/06-facebook.svg" alt="Facebook logo" /></a>
          <a href="https://www.instagram.com/tedxuofw/" target="_blank" class="social-bubble"><img src="/static/38-instagram.svg" alt="Instagram logo" /></a>
          <a href="https://www.youtube.com/channel/UCGmFbWHkkgWwA8iw9Ap11vw" target="_blank" class="social-bubble"><img src="/static/18-youtube.svg" alt="Youtube logo" /></a>
        </div>
        <!-- <button @click="$router.push('/login')">Get your tickets now</button> -->
      </div>
    </div>
    <div class="sponsors">
      <h3 class="sponsor-message">TEDxUofW is made possible with the help of our sponsors below!</h3>
      <div class="icons">
        <a href="https://wsecu.org/" target="_blank" class="sponsor-redirect"><img style="max-width: 10vw" src="/static/wsecu_logo.png"></a>
        <a href="http://www.roverdeja.com/" target="_blank" class="sponsor-redirect"><img style="max-width: 10vw" src="/static/ppt_tips_logo.png"></a>
        <a href="https://www.wellsfargo.com/" target="_blank" class="sponsor-redirect"><img style="max-width: 10vw" src="/static/wells_fargo_logo.png"></a>
        <a href="https://hub.washington.edu/" target="_blank" class="sponsor-redirect"><img style="max-width: 10vw" src="/static/the_hub_logo.png"></a>
        <a href="https://www.washington.edu/alumni/" target="_blank" class="sponsor-redirect"><img style="max-width: 10vw" src="/static/uw_alum_association_logo.png"></a>
      </div>
    </div>
    <p class="small-license">This independent TEDx event is operated under license from TED ©2021 TEDxUofW</p>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: {
    footerMargin: {
      type: Boolean,
      default: true
    }
  }
};
</script>

<style lang="scss" scoped>
@import "@/styles/_variables.scss";
$footer-break: 1000px;
$footer-tiny-break: 515px;

.footer {
  display: flex;
  flex-direction: column;
  width: 100%;
  box-shadow: 0 1px 5px #0f0f0f;
  z-index: 100;

  background-color: white;
  padding: 32px 32px 5px;
  box-sizing: border-box;

  &.footer-margin {
    margin-top: 64px;
  }

}

.social-bubbles {
  display: flex;
  justify-content: space-between;
  width: 120px;

  .social-bubble {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 25px;
    height: 25px;
    border-radius: 20px;
    text-decoration: none;
    background-color: black;

    &:hover {
      filter: brightness(80%);
    }

    img {
      height: 60%;
    }
  }
}

.small-license {
  font-size: 0.7em;
  line-height: 21px;
  margin: 0px;
  padding: 0px;
  text-align: center;
}

.our-logo {
  width: 120px;
  padding: 10px 0px;
}

.main-part {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px 0px 25px;
}

.sponsors {
  display: flex;
  flex-direction: column;
  align-items: center;

  .sponsor-message {
    text-align: center;
    margin: 0px;
    padding: 0px;
    font-size: 20px;
  }

  .icons {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    height: 15vw;
    width: 100%;
    margin-top: 20px;
    margin-bottom: 10px;

    .sponsor-redirect {
      width: 10vw;
    }
  }
}

.our-name {
  text-align: center;
  margin: 0px;
  padding: 0px;
  padding-bottom: 25px;
  font-size: 28px;
  font-weight: 900;
  color: $color-primary;
}

.our-event-date {
  text-align: center;
  font-size: 20px;
  margin: 0px;
  padding: 0px;
  line-height: 1.1em;
}

</style>
