# 6 ways to center a CSS block inside its parent
Example:

![css-center-block](https://github.com/girls-incode/css-center-align-blocks/blob/master/css-align-block-vertical-horizontal-2.jpg "css center block")

Add the blocks in index.html and give the base style for parent & child in app.css
```css
html, body {
    margin: 0;
    padding: 0;
}
.main {
    width: 40%;
    height: 40%;
    padding: 10px;
    margin: 5px auto;
    background-color: #dedede;
    border: 1px solid #000;
}
.inner {
    width: 30%;
    margin: 0 auto;
    padding: 10px;
    background-color: #fff;
    border: 2px solid #050;
}
```
Now let's center the inner block inside the main:

## 1. CSS absolute and relative positioning
```css
.case1 {
    position: relative;
}
.case1 .inner {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```
## 2. CSS box property
```css
.case2 {
    display: -webkit-box;
    -webkit-box-pack: center;
    -webkit-box-align: center;
}
```
## 3. CSS flex
```css
.case3 {
    display: flex;
    align-items: center;   // horizontal
    justify-content: center;  // vertical
}
```
## 4. CSS grid
```css
.case4 {
    display: grid;
    place-items: center;
}
// or
.case4 {
    display: grid;
    grid-template-columns: 1fr;
    align-items: center;
    justify-content: center;
}
```
## 5. CSS table
```css
.case5 {
    display: table;
}
.case5 .inner {
    display: table-cell;
    text-align: center;
    vertical-align: middle;
}
```
## 6. CSS inline display
```css
.case6 {
    text-align: center;
}
.case6 .inner {
    display: inline-block;
    margin: auto;
}
```
