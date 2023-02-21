### flex:多列自适应布局
			flex-container:设置display:flex的元素
			flex-item:flex-container内在文档流中的直接子元素，包括float元素
			main-axis:主轴，flex-item的排列方向
			cross-axis:辅轴，与main-axis垂直的方向
			
			flex-direction:
				row(default)|row-reverse|column|column-reverse 行排列还是列排列
			flex-wrap:no-wrap(default)|wrap|wrap-reverse
				元素是否放弃收缩，换行显示
			flex-flow:
				<'flow-direction'>||<'flex-wrap'> 值缩写
			order:<integer> initial 0
				设置flex-item，flex-item的排列顺序
			flex-basis:main-size|<width>
				设置flex-item的初始宽/高，main-axis方向
			flex-grow:<number> initial 0
				设置flex-item，拉伸权重，将空余空间按比例分配
			flex-shrink:<number> initial 0
				设置flex-item，收缩权重，将空余空间按比例分配
			flex:<'flex-grow'>||<'flex-shrink'>||<'flex-basis'>
				值缩写

			flex对齐
				justify-content:flex-start(default)|flex-end|center|space-between|space-around
					设置flex-container，主轴方向的剩余空间如何安排，flex-item的对齐方式
				align-items:flex-start(default)|flex-end|center|baseline|stretch
					设置flex-container，辅轴方向的剩余空间如何安排，flex-item的对齐方式
				align-self:auto(default)|flex-start|flex-end|center|baseline|stretch
					设置flex-item，设置单个flex-item在cross-axis上的对齐方式
				align-content:flex-start(default)|flex-end|center|space-between|space-around|stretch
					设置flex-container，出现多行时，在cross-axis上的剩余空间如何安排

### grid
	display:grid; inline-grid;
	grid-template-columns:; 数值方向各列宽度
	grid-template-rows:; 水平方向各行高度   容器有高度, rows会自动分配
	fr  以fr瓜分剩余内容

	grid-column: 1/4; // grid-item设置, 横跨1-3, 不包括4

### gird实现水平垂直居中
	{
		display:grid;
		justify-items:center;
		align-items:center;
	}

	//or
	.box{
		display:grid;
	}
	.child{
		justify-self:center;
		align-self:center;
	}


### inline-block实现水平垂直居中

		// html
		<div class="parent">
			<div class="align"></div>
			<div class="child"></div>
		</div>

		// css
		.parent
			height: 500px;
			text-align: center;
			background-color: #ccc;
			.align{
				visibility: hidden;
				display: inline-block;
				width: 1px;
				height: 100%;
				vertical-align: middle;
			}
			.child{
				display: inline-block;
				vertical-align: middle;
			}
		}



