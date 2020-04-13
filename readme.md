# vuepress-plugin-rss-feed

Generate `rss.xml` file with `content:encoded`

## Usage

```bash
npm i vuepress-plugin-rss-feed -D
```

Add plugin to your `.vuepress/config.js`

```js
module.exports = {
  plugins: [
    // other plugins
    [
      'rss-feed',
      {
        username: 'Bougie',
        hostname: 'https://www.bougieblog.cn',
        selector: '.content__post', // extract content to content:encoded
        count: 10,
        filter: (page) => /^blog/.test(page.relativePath),
      },
    ],
  ],
}
```

## License

[MIT](./LICENSE)
