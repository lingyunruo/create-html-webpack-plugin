## 同步生成html的webpack插件

```js
// 例子
new CreateHtmlWebpack({
    // js入口，对应模版的绝对路径
    templateMap: {
        'abc/efg/index': '/user/lib/index.html'
    },
    // 此参数可选, 在插入css之前进行一些操作，参数是模版的cheerio对象
    beforeAppendCss: function($) {
        $('head').append('<link>我自定义的一些东西</link>');
    },
    // 此参数可选, 在插入js前进行一些操作，参数是模版的cheerio对象
    beforeAppendJs: function($) {
        $('body').append('<script>也是我自己定义的</script>');
    }
});
```