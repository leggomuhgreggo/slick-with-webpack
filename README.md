## Slick with webpack

`yarn start` or `npm start` will runs the dev server at localhost:9000

Key think is to use [expose-loader](https://github.com/webpack-contrib/expose-loader) to serve jquery in the global object like:

```js
{
  test: require.resolve("jquery"),
  use: [
    {
      loader: "expose-loader",
      options: "$"
    }
  ]
}
```
