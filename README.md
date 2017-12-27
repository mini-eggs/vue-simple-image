# Just another progressive image component for Vue.

#### Why

This is made for the uses case of having 15+ very large images on the page with users transitioning on and off the page frequently. This solves the use case of very expensive images being downloaded after they are no longer need. After an image is no longer needed its request is cancelled unlike default <img /> tags.

#### Installing

`$ npm install vue-simple-image`

#### Example

```html
<template>
  <section>
    <h1>My cool meme! :-)</h1>
    <simple-image src="https://media.makeameme.org/created/javascript-sgfi8v.jpg" :onComplete="handleComplete" :onFail="handleFail" />
  </section>
</template>

<script>
import SimpleImage from "vue-simple-image";

export default {

  components: { SimpleImage },

  methods: {

    handleComplete() {
      // Silence is golden.
    },

    handleFail(err) {
      // console.log(err)
    }

  }

};
</script>
```

#### Extra usage information

This NPM package does not have a build process in place. This will work with most default Vue builds (i.e. if you use Nuxt or the common Vue init CLI templates).
