# vue-contextmenu-ui
this is contextmenu components
## 组件使用示例:
#### template代码:
```
<menuCom :id="'custom_menuwarp'" :page="pagePosition" :visble.sync="visble">
  <div style="height:150px;width:100px;background:white;color:black;border-radius:4px">
  ....
  </div>
</menuCom>
```

>>子组件依赖三个值分别是:id用于区分各实列的id:pagePosition:传入鼠标点击位置、visble:控制组件隐藏显示。
---

#### script代码:
>```import Menu from '@/components/menu'``` 
><br>```components:{Menu}```</br>
#### 控制函数(自定义区域侦听右击事件 @contextmenu.prevent.stop="showMenu($event)" ):
```
data(){
  return {
    pagePosition:{},
    visble:false
  }
},
methods:{
  //右击菜单
  showMenu(ev){
    this.pagePosition = {pageX : ev.pageX , pageY : ev.pageY};
    this.visble = true
  }
}
```

