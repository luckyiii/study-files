## 小程序--textarea多行输入框自适应

使用了auto-height属性：是否自动增高，设置auto-height时，height不会生效。

index.wxml

```
<view class="container">
  <view class="list-item">
    <view class="left">学习心得：</view>
    <view class="right">
      <textarea auto-height="true" placeholder="请输入文字" maxlength="500"></textarea>
    </view>
  </view>
</view>
```

index.wxss

```
.container {
  margin: 0;
  padding: 0;
}
//外层高度自适应
.list-item {
  margin-top: 20rpx;
  margin-left: 20rpx;
  width: 100%;
  height: auto;
  border: 6rpx solid blueviolet;
}
.left {
  float: left;
  line-height: 100rpx;
}
//右边部分，高度自适应，最小高度设为100rpx
.right {
  height: auto;
  min-height: 100rpx;
  display: flex;
  align-items: center;
}
.right textarea {
  width: 500rpx;
  border: 5rpx solid yellowgreen;
}
```

效果展示：

<img src="C:\Users\wrm\AppData\Roaming\Typora\typora-user-images\1597928718904.png" alt="1597928718904" style="zoom:50%;" />

<img src="C:\Users\wrm\AppData\Roaming\Typora\typora-user-images\1597928850584.png" alt="1597928850584" style="zoom:50%;" />