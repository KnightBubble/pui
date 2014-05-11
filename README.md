#PUI

PUI是拍拍前端的UI组件框架，用于实现页面上的交互效果。

##why use PUI

写这个框架的目的，是为了从代码层面上规范UI组件代码。让开发者不再关注插件如何生成，抽象了一系列的重复任务。开发者仅需要实现具体的业务逻辑，其他则交给PUI完成。

PUI 解决了大量基础性问题，有助于提高效率，有利于代码重用， 非常适合用来创建有状态的插件。

其核心代码主要参考jQuery UI的实现，其API与jquery ui 基本一致。如果你熟悉jQuery ui的使用，那么相信你会很快熟练掌握PUI

1. 生成命名空间（如果需要）和属性
2. 避免在相同元素下widget的多实例化。即同一个dom下只实例化一次，并将插件对象缓存在dom上方便后续调用。
3. 链式的转发回调插件
4. 限制私有方法被外界调用

###Getting Started

####创建一个插件
```js
Pui.widget('pp.plugin',{
    _create:function(){
        console.log('hello work');
    }
    //your code
})
```
调用方法：
```js
$('#ID').plugin();
```

非常简单吧。

###环境依赖
* git
* node(包括npm)
* grunt (npm install -g grunt-cli)
* bower (npm install -g bower)


###feekback
如果您有任何关于PUI的问题，可以通过[git issue](https://github.com/baofen14787/pui/issues)给我反馈bug，我会尽快解决。


### Changelog
* v0.1 项目创建

### Other
[My Blog](http://www.ghugo.com)