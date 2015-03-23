# Fly
demo: http://codepen.io/hzxs1990225/full/ogLaVp

In your web page:

```html
<script src="jquery.js"></script>
<script src="dist/jquery.fly.min.js"></script>
<script>
jQuery(function($) {
  $('#fly').fly({
    start:{
      left: 11,  //开始位置（必填）#fly元素会被设置成position: fixed
      top: 600,  //开始位置（必填）
    },
    end:{
      left: 500, //结束位置（必填）
      top: 130,  //结束位置（必填）
      width: 100, //结束时高度
      height: 100, //结束时高度
    },
    autoPlay: false, //是否直接运动,默认true
    speed: 1.1, //越大越快，默认1.2
    vertex_Rtop：100, //运动轨迹最高点top值，默认20
    onEnd: function(){} //结束回调
  });
  $('#fly').play(); //autoPlay: false后，手动调用运动
  $('#fly').destroy(); //移除dom
});
</script>
```
IE10以下，引入src/requestAnimationFrame.js

@support IE>=7




