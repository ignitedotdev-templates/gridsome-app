<template>
  <Layout>
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->

    <main>
      <div class="">
        <g-image alt="Example image" src="~/favicon.png" width="135" />
        <!-- <img src="{logo}" alt="logo" className="logo" /> -->
      </div>
      <div class="container">
        <div class="inner-container">
          <h2 class="header">
            You’ve just ignited a new
            <span class="library"> Gridsome </span> static site!
          </h2>
          <span class="pathname"> {{ currentPath }} </span>
        </div>
        <p class="footer">Made in Nigeria with 💖</p>
      </div>
    </main>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Hello, world!",
  },
  data() {
    return {
      currentPath: "",
    };
  },
  mounted() {
    this.currentPath = window.location.href;
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}

main {
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 7px;
  align-items: center;
  justify-content: center;
}
.logo {
  width: 200px;
  height: 200px;
}
.container {
  display: flex;
  flex-direction: column;
  text-align: center;
  gap: 10px;
}
.inner-container {
  display: flex;
  flex-direction: column;
  line-height: 1;
}
.header {
  font-size: 36px;
  font-weight: 400;
  color: #344054;
}
.pathname {
  color: #004eeb;
  font-size: 20px;
}
.footer {
  font-size: 20px;
  font-weight: 500;
  color: #344054;
}
.library {
  color: #00a672;
  font-weight: 600;
  margin-left: 10px;
  margin-right: 10px;
}
</style>
