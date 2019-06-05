# less-plugin-dls

Less plugin for Baidu DLS.

🚧 This is a work in progress. 🚧

## Installation

```sh
npm i --save-dev less-plugin-dls
```

## Usage

### Autoinject with Less plugin

```js
import less from 'less'
import dls from 'less-plugin-dls'

less
  .render('a { color: @dls-link-font-color-normal; }', {
    plugins: [dls()]
  })
  .then(result => {
    // handle result
  })
```

### Import from stylesheets

With [less-loader](https://github.com/webpack-contrib/less-loader):

```less
@import "~less-plugin-dls/tokens/index.less";

a { color: @dls-link-font-color-normal; }
```

### Use CLI argument

```sh
lessc style.less --dls
```

## License

[MIT](https://github.com/ecomfe/less-plugin-dls/blob/master/LICENSE)
