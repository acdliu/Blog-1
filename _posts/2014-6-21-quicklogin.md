quicklogin工具
=====

@(tool)[工具|quicklogin]

## 背景

在做手Q开发的时候，总会有些特别的需求要求输入账号和密码。比如：

- 重新安装的时候，账号数据会丢失，之前保留的账号信息也丢失，这样就要输入账号和密码
- 一些特别的需求，需要切换账号
- 有些号码不是自己的，没法记这么多QQ号码和密码
- 重复性非常大

且在你完成登陆动作后你已经做了：

1. 输入账号
2. 输入密码（这个过程密码不可见，可能输错）
3. 点登陆按钮

等这些问题烦恼。于是就想办法代替这些烦恼的操作，只需告诉他我要登陆这个账号，输入账号和密码会自动完成以上动作。简单就是：

1. 选择一个账号登陆就可以了

于是，就有了以下这个工具。
工具的思路大致描述是：

- 在app的Debug页面放入口
- 从入口进入页面，读取sd卡某个文件，文件中存有账号信息和密码信息，然后listview展示给用户。
- 页面属性是设置唯一的，也就是即使重复进入该页面，进入的是同一个。
- 选中某一个账号就调用登陆借口，提供账号密码过去即可。

工具是不是很简单，重在idea，重在方便了开发。