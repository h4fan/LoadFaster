# LoadFaster
Load faster on client side by redirecting or blocking domains
## 问题
你是否遇到这样的情况，明明网速还不错，但是网页打开就是很慢？
查看网络请求，发现：
* 一些字体请求你无法访问，但是浏览器却一直在那里等待
* 一些第三方js，使用的cdn是在你这里很慢，所以浏览器一直在那里转圈

那么我们有没有办法解决呢？

## 原理
通过chrome插件的declarativeNetRequestWithHostAccess功能，对特定的请求进行redirect或者block，达到更快的访问。
我们通过在客户端，使用chrome插件，对特定的请求进行处理，来达到更快访问的目的。
比如：
* 字体访问不到？直接block
* cdn js加载慢？redirect到一个更快的cdn

## 使用访问
* 使用开发者模式加载loadfaster插件。
* 在rules.json中增加自定义的规则。
* 更新插件
* 快速访问

规则可以参考[declarativeNetRequest#rules](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API/declarativeNetRequest#rules)
样例可以参考[dnr-redirect-url](https://github.com/mdn/webextensions-examples/blob/main/dnr-redirect-url/redirect-rules.json)
