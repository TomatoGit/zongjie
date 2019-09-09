#  闭包
```JavaScript
function foo(){
    var a=2;
    
    function bar(){
        console.log(a);
    }
    
    return bar;
}

var baz=foo();
baz();  //2  闭包的效果
```
在foo()执行之后，通常会期待整个foo()的内部作用域都被销毁（垃圾回收机制）。  
而闭包可以阻止这件事情的发生，因为内部函数bar()还在使用这一作用域。  
bar()持有对foo()内部作用域的引用，而这个引用就是**闭包**   
#### 当内部函数记住并访问当前作用域时就产生了闭包，而此函数对当前部作用域的引用就叫闭包