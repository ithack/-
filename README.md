无缝滚动方法，用前引入JQuery文件

html布局：
<div class="box">
    <span class="prev">
        上一张
    </span>
    <dl id="roll">
        <dd>
            <img src="images/1.jpg" />
        </dd>
        <dd>
            <img src="images/2.jpg" />
        </dd>
        <dd>
            <img src="images/3.jpg" />
        </dd>
        <dd>
            <img src="images/4.jpg" />
        </dd>
    </dl>
    <span class="next">
        下一张
    </span>
</div>
调用：
$(document).ready(function() {
 
    $("#roll").parallelRoll({
        boxName: "box",
	      //最外层盒子类名
	      tagName: 'li',
	      //滚动标签元素
	      time: 3000,
	      //滚动间隔时间
	      direction: 'false',
	      // 动方向  right-->向右    left-->向左    false-->手动滚动
	      visual: 5,
	      //可视数
	      prev: "prev",
	      //向上
	      next: "next",
	      //向下
	      amount: 1 // 滚动数  默认是1
    });
 
});
