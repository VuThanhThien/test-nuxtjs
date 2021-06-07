<template>
  <div class="body theme" id="body" ref="body">
    <div class="navbar">
        <button id="light"  @click="lightMode">light</button>
        <button id="dark" @click="darkMode">dark</button>
    </div>
    <div class="main">
      <p>
        Trysail Sail ho Corsair red ensign hulk smartly boom jib rum gangway.
        Case shot Shiver me timbers gangplank crack Jennys tea cup ballast
        Blimey lee snow crow's nest rutters. Fluke jib scourge of the seven seas
        boatswain schooner gaff booty Jack Tar transom spirits.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    darkMode() {
      console.log(this.$refs.body.classList[1]);
        // this.$refs.body.classList.pop();
        // this.$refs.body.classList.add("dark");
      this.$refs.body.classList.replace("theme", "dark");
      this.$refs.body.classList.replace("light", "dark");
    },
    lightMode() {
      this.$refs.body.classList.replace("theme", "light");
      this.$refs.body.classList.replace("dark", "light");
    },
  },
};
</script>

<style lang="scss" scoped>
body {
  margin: 0;
  padding: 0;
  font-family: "Montserrat", sans-serif;
  color: var(--text);
  background: var(--bg);
}

.main {
  min-height: 1000px;
  padding: 2rem;
  background-color: var(--bg-solar);
  color: var(--text);
}

.navbar {
  width: 100%;
  background: var(--bg-nav);
  color: var(--text);
  display: flex;
  justify-content: center;
  button{
    background-color: var(--gray1);
    margin: 10px;
    border: none;
    width: 100px;
    height: 50px;
    border-radius: 5px;
  }
}
.navbar-nav {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  height: 100%;
}

</style>