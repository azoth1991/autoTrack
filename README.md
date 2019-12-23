# autoTrack

> 仓库地址：https://github.com/azoth1991/autoTrack

实现了一个轻量级埋点组件，目前只实现了页面埋点和点击埋点。
### 使用方法
引入
```
import autoTrack from './AutoTrack.js';
```
调用
```
autoTrack({
  pageCallback: this.pageCallback, // 页面埋点回调
  eventCallback: this.eventCallback, //点击埋点回调
});
```
页面插入埋点信息:  
1、在组件上需要埋点的位置加入logpage  
2、在点击事件onClick同级写上logevent
```
<div className="App" logpage={{type:'logPage'}}>
    {arrData.map(v=>{
      return <div className="item" onClick={this.handleClick} logevent={{type:'logEvent', key:v}} key={v}>{v}</div>
    })}
</div>
```

### 效果

![](https://user-gold-cdn.xitu.io/2019/3/25/169b56dd5c4577da?w=1576&h=1072&f=gif&s=1751464)

### 展望
打算加入曝光埋点
