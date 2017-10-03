# Css_precompiler-sass(css预编译处理sass)

**执行&运行**
```
sass --watch sass:css    //实时编译
sass --watch sass:css --style compact  //css输出格式为紧凑格式
sass --watch sass:css --style compressed  //css输出格式为压缩格式
sass --watch sass:css --style expanded  //css输出格式为拓展格式
```

*嵌套*
```
body{
    font: {
        family:Helvetica;
        size: 15px;
        weight:normal; 
    }
}
```

*定义变量*
```
@mixin alert($text-color,$background) {
  color: $text-color;
  background-color: $background;
  a {
    color: darken($text-color,10%);
  }
}
.alert-warning{
    @include alert(#8a6d3b,#fcf8e3);
}
.alert-info{
    @include alert($background:#d9edf7,$text-color:#31708f)
}
extend的写法
.alert {
    padding: 15px;
    margin: 5px;
    font-size: 20px;
}
.alert-info{
    @extend .alert;
    background-color: #d9edf7;
}
```

*继承*
```
.alert{
    padding: 15px;
    margin: 5px;
    font-size: 20px;
}
.alert a{
    font-weight: bold;
}
.alert-info{
    @extend .alert;
    background-color: #d9edf7;
}
```
