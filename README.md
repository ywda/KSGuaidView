# App新特性页面
<br/>
<span id = "pic1">

![图一](https://github.com/iCloudys/KSGuaidView/blob/master/Gif/QQ20170531-143315.gif)<br/><br/>

</span>
<span id = "pic2">

![图二](https://github.com/iCloudys/KSGuaidView/blob/master/Gif/QQ20170531-143634.gif)<br/><br/>
</span>

使用方法很简单，直接把KSGuaidView文件夹拖到工程,<br/>然后稍微修改一下文件夹内的```KSGuaidProperty.plist```内容即可<br>
<br/>
--------- 
## KSGuaidProperty.plist文件介绍:<br/><br/>
 * ```kImageNamesArray```
<br/>

         图片数组的Key,值是一个NSArray<br/> 
         里面包含了要显示新特性的图片的名字，<br/>
         这些图片需要添加在Assets.xcassets目录内。<br/><br/>
 
 * ```kLastNullImageName```
 
<br/>

         如果要实现最后一张图片滑动去除的效果[如图二](#pic2),<br/>
         需要在上一个key里面的数组最后添加这个key作为最后一张图片的name。<br/>
         注意:如果用这种方式退出，是不会显示"立即体验"类似的按钮。<br/><br/>

 
* ``` kHiddenBtnImageName```

<br/>

         "立即体验"按钮的图片名称，如果想在最后一张图片上添加一个体验按钮 [如图一](#pic1),<br/>
         则需要指定这个图片的名字，按钮大小会跟随图片的大小设定。<br/>
         如果在`kImageNamesArray`最后添加了 `kLastNullImageName` ，<br/>
         即使指定了`kHiddenBtnImageName`不过也不会起作用。<br/><br/>

 
*  ```kHiddenBtnCenter```

<br/>

         "立即体验"按钮的相对屏幕的位置，value是`{x,y}`字符串类型的point。<br/>
         `x,y`的取值范围为[0,1],`例如 {0.5,0.5} 是屏幕中心。<br/>

