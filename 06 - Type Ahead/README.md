# 06 - Type Ahead


> [javascript30](https://javascript30.com/) 是 [Wes Bos](https://github.com/wesbos) 发起的一个30天JS编码挑战，30个教学30天完成30个前端小项目，无需引入额外框架，无需编译，无第三方库，无开发模板，回归纯粹的Javascript开发。
> 
> 作者该项目的 → [GitHub](https://github.com/soyaine/JavaScript30)


## 实现效果
1. 一个输入框，跟随其后的模拟折纸样式的输入提示列表。

2. 实现预输入联想，通过在输入控件上的操作弹出匹配到的联想结果，并高亮显示匹配词。

![](http://p1.bpimg.com/567571/04e4c5d7ea17e2f4.jpg)

## 知识点

### CSS

#### [box-sizing](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing)
> box-sizing 属性用来改变默认的 CSS 盒模型 对元素宽高的计算方式。

```
html {
    box-sizing: border-box;
    ...
}
```
`border-box` 容器宽高包括了 border 与 pading， 尺寸计算公式：width = border + padding + 内容的宽度，height = border + padding + 内容的高度。

#### [box-shadow](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow)
> `box-shadow` 以逗号分割列表来描述一个或多个阴影效果。

 ```
input.search {
    ...
    box-shadow: 0 0 5px rgba(0, 0, 0, .12), inset 0 0 2px rgba(0, 0, 0, .19)
}
```
```
none | [inset? && [ <offset-x> <offset-y> <blur-radius>? <spread-radius>? <color>? ] ]#
```
`inset` 为内阴影。

#### [justify-content](https://developer.mozilla.org/zh-CN/docs/Web/CSS/justify-content)
> `justify-content` 属性定义了浏览器如何分配顺着父容器主轴的弹性元素之间及其周围的空间。
```
.suggestions li {
    ...
    justify-content: space-between;
    ...
}
```
`space-between` 致使均匀排列每个元素，首个元素放置于起点，末尾元素放置于终点。项目中的效果为地名和人口数量分别置于左右贴边。


