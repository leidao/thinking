# thinking
## vus
### vue的双向绑定的原理是什么？
```
 Vue是采用数据劫持加发布-订阅模式的方法，在初始化data的时候，会使用es5的.Object.defineProperty重新定义对象的属性，给每个属性添加getter和setter方法（数据劫持），当页面使用对应属性时，会触发getter进行依赖收集（watcher），当给对应属性赋值时，会触发setter通知对应的依赖进行更新（发布订阅）
```
