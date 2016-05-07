# vue-helmet

A HTML head manager for Vue, edit the page title easily!

# Instllation

### Browser globals

> The **dist** folder contains `vue-helmet.js` and `vue-helmet.min.js` with the component exported in the `window.VueHelmet` object. 

```html
<script src="path/to/vue.js"></script>
<script src="path/to/vue-helmet.js"></script>
<script>
    Vue.use(VueHelmet);
    var vm = new Vue({
        el: "body"
    });
</script>
```

### NPM

```shell
$ npm install --save vue-helmet
```

## CommonJS

```js
var VueHelmet = require('vue-helmet/dist/vue-helmet.common.js');

new Vue({
  components: {
    'vue-helmet': VueHelmet
  }
})
```

## ES6

```js
import VueHelmet from 'vue-helmet/dist/vue-helmet.common.js'

new Vue({
  components: {
    VueHelmet
  }
})
```

# Example

```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>vue-helmet</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Something old." />
</head>

<body>
  <vue-helmet :html-attributes="{'lang': 'zh-CN'}"
              title="New Title Here"
              :base="{'target': '_blank', 'href': 'http://a.d.c'}"
              :meta="{'description': 'New Description Here.'}"
              :links="[{'rel': 'canonical', 'href': 'http://a.b.c'}]"
              ></vue-helmet>
  <div>Hello World!</div>
  <script type="text/javascript" src="/dist/vue.js"></script>
  <script type="text/javascript" src="/dist/vue-helmet.js"></script>
  <script>
    Vue.use(VueHelmet);
    var vm = new Vue({
      el: "body"
    });
  </script>
</body>

</html>
```

# Props

| Prop | Type | Example |
| ---- | ---- | ------- |
| html-attributes | Object | `:html-attributes="{'lang': 'zh-CN'}"` |
| title | String | `title="New Title Here"` |
| base | Object | `:base="{'target': '_blank', 'href': 'http://a.d.c'}"` |
| meta | Object | `:meta="{'description': 'New Description Here.'}"` |
| links | Array | `:links="[{'rel': 'canonical', 'href': 'http://a.b.c'}]"` |