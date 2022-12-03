# Nuxt ESLint Config

## Usage

Add this package to your devDependencies
```bash
$ npm i -D https://github.com/wiopriph/eslint-config
```

Install `eslint` and `prettier`
```bash
$ npm i -D -E eslint@7.30.0 @nuxtjs/eslint-config@6.0.0 @nuxtjs/eslint-module@3.0.2 \
eslint-formatter-gitlab@2.2.0 eslint-plugin-wdio@7.4.2 eslint-plugin-vue@7.16.0 \ 
prettier@2.3.2 eslint-config-prettier@8.3.0 eslint-plugin-prettier@4.0.0
```

Configure nuxt.config.js
```js
import nuxtConfig from '@wiopriph/eslint-config/src/nuxt-config';

export default {
  extend(config, { isClient, isDev }) {
    nuxtConfig({ isClient, config, isDev });
  }
}
```

Create a `.eslintrc` file

Extend our config:
```json
{
  "extends": [
    "@wiopriph/eslint-config"
  ]
}
```

Configure .prettierrc.js (for prettier)
```js
module.exports = {
  ...require('@wiopriph/eslint-config/src/prettier-config'),
};
```
