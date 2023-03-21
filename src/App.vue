<template>
  <h1 class="title">All AAX victims can join lawsuit</h1>

  <div class="bg">
    <div class="circle"></div>
    <div class="circle2"></div>
    <svg>
      <filter id="wave">
        <feTurbulence x="0" y="0" baseFrequency="0.009" numOctaves="5" seed="2">
          <animate attributeName="baseFrequency" dur="30s" values="0.02;0.005;0.02" repeatCount="indefinite" />
        </feTurbulence>
        <feDisplacementMap in="SourceGraphic" scale="30" />
      </filter>
    </svg>
  </div>


  <div class="contact">
    <p>Teegram-group: <a href="https://t.me/aaxinvestigation" target="_blank">https://t.me/aaxinvestigation</a></p>

    email: <a href="mailto:aaxuser.rights@gmail.com">aaxuser.rights@gmail.com</a>
  </div>
</template>

<script setup>

</script>

<style lang="scss">
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
  overflow: hidden;
  text-align: center;

  background: #111;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.bg {
  z-index: 0;
  position: absolute;
  left: 50%;
  transform: translate(-50%);
}

.circle {
  position: relative;
  height: 500px;
  width: 500px;
  filter: url(#wave);
  animation: rotate 30s linear infinite;

  &::before {
    content: "";
    position: absolute;
    top: 100px;
    left: 100px;
    right: 100px;
    bottom: 100px;
    border: 10px solid #fff;
    border-radius: 50%;
    box-shadow: 0 0 50px #fff, inset 0 0 50px #fff;
    filter: url(#wave) blur(10px);
    animation: anim 4s linear infinite;
  }
}

@keyframes anim {
  0% {
    box-shadow: 0 0 50px #fff, inset 0 0 50px #fff;
  }

  20% {
    box-shadow: 0 0 50px rgba(255, 0, 0, 0.496), inset 0 0 50px #f00;
  }

  40% {
    box-shadow: 0 0 50px #ff0, inset 0 0 50px #ff0;
  }

  60% {
    box-shadow: 0 0 50px #0ff, inset 0 0 50px #0ff;
  }

  80% {
    box-shadow: 0 0 50px rgba(255, 0, 255, 0.631), inset 0 0 50px #f0f;
  }
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

svg {
  display: none;
}

.title {
  font-size: 56px;
  color: #fff
}

.contact {
  position: relative;
  z-index: 9;
  margin-top: 48px;
  padding: 16px;
  text-align: left;
  background: #fff;
  border-radius: 8px;
}
</style>
