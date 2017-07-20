# dropDown

下拉加载H5+WEB版本

## 下拉加载(持续更新react和vue组件版)

* 不依赖任何JS库,支持移动端和PC端,支持所有主流浏览器
* 直接引用dropDown.js既可以使用

## 不定期更新一下版本

* 下拉视差动画版本
* react组件版本
* vue组件版本

## 初始化调用方法(增加定时器模拟,实际开发可以剔除)

```js
var drop = new drops(document.body,function(){
	var timer = setTimeout(function () {
        clearTimeout(timer);
        i++;
        alert("下拉已经刷新, Do someThing")
    	drop.pullToRefreshDone();
    }, 500);
});
```

## React 调用方法


```js
import Drop from './drop'

export default class Index extends Component {

	constructor(props) {
		super(props)

		//数据请求回调callback
        this.fetch = (call)=>{
            console.log("111")
            setTimeout(()=>{
                call()
            },9000)
        }
 
	}

	render() {
		
		return (
			<div className={`index need`}>
                <Drop run={this.fetch}/>
			</div>		
			
		)
	}
}
```



