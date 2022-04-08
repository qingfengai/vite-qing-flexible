<!--
 * @Date: 2022-04-08 09:08:07
 * @Description: 
-->
# vite-qing-flexible

Vite plugin that automatically injects flexible scripts and converts pixel units to rem units

### Install

```bash
$ npm i vite-qing-flexible -D
# or
$ yarn add vite-qing-flexible -D
```

### Usage

Config plugin in vite.config.ts

```javascript
import { defineConfig } from 'vite';
import flexible from 'vite-qing-flexible';

export default defineConfig({
  plugins: [
    flexible(),
  ]},
});
```


Flexible scripts are automatically injected into the head

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Will be generated automatically -->
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,viewport-fit=cover"
    />
    <script>
    // flexible script
    </script>
  </head>
  <body></body>
</html>
```

### Resource

- https://github.com/cuth/postcss-pxtorem
- https://github.com/posuihushui/flexible.js
