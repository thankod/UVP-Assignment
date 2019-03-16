# FastReserach Team HomeWork
## ScrollViewer

### Reason:
> 因为我们将要做的Project是为科研工作者服务的。因此需要一个能够支持垂直滚动的控件来做到阅读论文、笔记以及浏览自己管理的命令行参数(一个页面显示不全)等。
### Platform:
> IOS by Swift

### examples
>由于ios storyboard的方便性。因此我们在创建ios工程后 在控件区搜索UIScorollView
![Alt text](1.png)
拖动到UI中
![Alt text](2.png)
添加约束
![Alt text](3.png)
添加view控件
![Alt text](4.png)
修改view控件的高度以及添加约束
![Alt text](6.png)
添加两个button
![Alt text](7.png)
运行后的效果:\
![Alt text](8.gif)
## NavigationView

 ### Reason:
> 基本上所有Project是包含导航的，能够起到快速查找所需要的信息并且使程序结构贬的清晰。于是我们选择用NavigationView这个组件来进行导航，它基本满足了我们对导航需要的所有需求，能够进行界面之间的跳转并且能够做到弹放导航框。
### Platform:
>Wechat mini-program
### Code:
<script>
import wepy from 'wepy';
import 'wepy-async-function';
 export default class extends wepy.app {
    config = {
        pages: ['pages/test1', 'pages/test2'],
        window: {
            backgroundTextStyle: 'light',
            navigationBarBackgroundColor: '#fff',
            navigationBarTitleText: '实验程序',
            navigationBarTextStyle: 'black'
        },
        tabBar: {
            list: [{
                pagePath: "pages/test1",
                text: "界面1",
                iconPath: "pages/icon.png",
                selectedIconPath: "pages/test1/selectedIcon.png"
            }, {
                pagePath: "pages/test2",
                text: "界面2",
                iconPath: "pages/icon.png",
                selectedIconPath: "pages/test2/selectedIcon.png"
            }],
            selectedColor: "#09bb07"
        },
        debug: true
    }

     onLaunch() {
        wx.getSystemInfo({
            success(data) {
                console.log(data)
            },
            fail() {
                console.log("fail")
            }
        })
    }
}
</script>
