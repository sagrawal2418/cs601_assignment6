<template>
  <main>
    <section id="image-container">
      <img
        :src="hoverImage(this.image_one, this.image_five)"
        v-show="active"
        @mouseover="hover = true"
        @mouseleave="hover = false"
        width="400"
        height="400"
        alt="alphabet A"
      />

      <img
        :src="hoverImage(this.image_two, this.image_six)"
        v-show="active"
        @mouseover="hover = true"
        @mouseleave="hover = false"
        width="400"
        height="400"
        alt="alphabet H"
      />

      <img
        :src="hoverImage(this.image_three, this.image_seven)"
        v-show="active"
        @mouseover="hover = true"
        @mouseleave="hover = false"
        width="400"
        height="400"
        alt="alphabet G"
      />

      <img
        :src="hoverImage(this.image_four, this.image_eight)"
        v-show="active"
        @mouseover="hover = true"
        @mouseleave="hover = false"
        width="400"
        height="400"
        alt="alphabet U"
      />
    </section>
  </main>
</template>


    <script>
export default {
  name: "App",
  mounted() {
    let Script = document.createElement("script");
    Script.setAttribute(
      "src",
      "https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.14.1/lodash.min.js"
    );
    document.head.appendChild(Script);
  },
  data() {
    return {
      image_one: require("../assets/image_one.jpg"),
      image_two: require("../assets/image_two.jpg"),
      image_three: require("../assets/image_three.jpg"),
      image_four: require("../assets/image_four.jpg"),
      image_five: require("../assets/image_five.jpg"),
      image_six: require("../assets/image_six.jpg"),
      image_seven: require("../assets/image_seven.jpg"),
      image_eight: require("../assets/image_eight.jpg"),
      hover: false,
      active: true,
    };
  },
  /**Method invoked for mouse hover and mouse leave action*/
  methods: {
    hoverImage: function (image1, image2) {
      if (this.hover == true) {
        return image2;
      }
      return image1;
    },
  },
};
</script>