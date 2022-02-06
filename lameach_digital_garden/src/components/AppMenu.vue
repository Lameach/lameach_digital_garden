<template>
  <div class="menu-container">
    <img class="avatar" src="../assets/Avatar.png"/>
    <div class="my-name">
      <span class="name">Dan Botvinnikov </span>
      <span class="nickname">lameach</span>
    </div>
    <div class="social">
      <a class="sm-link" href="https://vk.com/d.botvinnikov" target="blank"><img src="../assets/vk_logo.svg"/></a>
      <a class="sm-link" href="https://github.com/Lameach" target="blank"><img src="../assets/gh_logo.svg"/></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppMenu'
}
</script>

<style>
.menu-container {
  background-color: #F0EFEC;
  grid-area: menu;
  border-right: 2px solid #A1A1A1;
  filter: drop-shadow(1px 0 2px rgba(0, 0, 0, 0.25));
  height: 100vh;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 2fr 1fr 2fr 2fr 1fr 2fr 1fr;
  grid-template-areas: 
  "."
  "avatar"
  "nick"
  "."
  "."
  "."
  "social"
  ".";
  cursor: pointer;
}

.menu-container:hover {
  filter: drop-shadow(2px 0 4px rgba(0, 0, 0, 0.4));
}

.avatar {
  grid-area: avatar;
  width: 101%;
  height: auto;
}

.my-name {
  font: var(--font-headers);
  font-size: 1.5rem;

  grid-area: nick;
  transform: rotate(-90deg);
  margin-top: 3vh;
  white-space: nowrap;
  height: fit-content;
  position: absolute;
  justify-self: center;
}
.name {
  width: fit-content;
  height: fit-content;
  color: #9C8C75;
  margin-right: 1vh;
}
.nickname {
  font-weight: bold;
  color: #493E2F;
}

.social {
  grid-area: social;
  align-self: end;
  justify-self: center;
}

.sm-link {
  display: block;
  width: 37.5%;
  height: auto;
  margin-top: 2vh;
}

.sm-link:hover {
  filter: brightness(0.8);
}

</style>