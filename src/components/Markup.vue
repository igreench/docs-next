<template>
  <app-code
    class="my-0"
    v-bind="$attrs"
  >
    <prism
      ref="code"
      :code="code"
    />
  </app-code>
</template>

<script>
  import 'markdown-it-prism'
  import 'prismjs/themes/prism.css'
  import 'prismjs/components/prism-bash'
  import 'prismjs/components/prism-css'
  import 'prismjs/components/prism-javascript'
  import 'prismjs/components/prism-json'
  import 'prismjs/components/prism-pug'
  import 'prismjs/components/prism-sass'
  import 'prismjs/components/prism-scss'
  import 'prismjs/components/prism-stylus'
  import 'prismjs/components/prism-typescript'

  export default {
    name: 'Markup',

    components: {
      Prism: () => import(
        /* webpackChunkName: "vue-prism-component" */
        'vue-prism-component'
      ),
    },

    props: { code: String },
  }
</script>
