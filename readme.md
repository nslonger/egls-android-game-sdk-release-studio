# egls-android-game-sdk-release-studio

尊敬的开发者您好：<br /><br />
从4.x.x版本起，我们采用了新的账号体系，所以并不兼容旧版（即同一个账号在登录后返回的uid与3.x.x版本的不一致）。如果您的游戏曾经接过旧版本的SDK，并且将要使用4.x.x版本的SDK时，请配合我们做游戏的强更及其他必要的更新操作（详情请咨询我方运营）。<br /><br />
### Version：4.3.72
1. constraint库升级到1.1.0版本（com.android.support.constraint:constraint-layout:1.1.0）；
2. 修改“用户协议”页面弹出流程。
### Version：4.3.66
将so打进aar中，便于同步更新，不再需要单独拷贝到工程进行替换（当需要选择so类型时，可在项目工程的build.gradle文件里添加配置，否则默认使用so全部类型）。
### Version：4.3.65
修复游客绑定功能异常问题，需更换同名so文件。
### Version：4.3.62
修复已知bug。
### Version：4.3.60
修复OneStore SDK v5版本的支付bug。
### Version：4.3.59
修复Tablet设备UI的适配问题。
### Version：4.3.58
韩国发行区Google推荐审核新要求适配。
### Version：4.3.56
修复已知bug。
### Version：4.3.52
1. 增加对新加坡发行的适配逻辑；
2. 将原有的“EGLS_SERVER_TYPE”字段修改为“EGLS_PUBLISHMENT_AREA”；
3. 分享接口目前改版中，原有的接口不再推荐使用，等新的分享接口发布后，旧版分享接口将被废弃;
4. 为了兼容Android API 27版本要求，修改“com.egls.socialization.google.play.GooglePlayActivity”的“screenOrientation”属性值为“behind”，修改“theme”属性值为“@style/EglsTheme.Translucent.NoTitleBar.Fullscreen.NoAnimation”。
### Version：4.3.49
修复游客账号绑定功能的bug。
### Version：4.3.45
修复悬浮菜单中“NaverCafe”按钮点击后无响应问题。
### Version：4.3.44
1. 部分bug修复；
2. 韩国发行区所使用的OneStore SDK版本升级到v5，AndroidManifest.xml文件中，去掉名为“com.skplanet.dodo.IapWeb”的Activity配置，增加名为“iap:view_option”的meta元素配置；其库文件引用变更为“iap_plugin_v17.01.00_20180206.jar”。
### Version：4.3.25
修复在部分设备上初始化崩溃的问题。
### Version：4.3.24
修复港台发行区MyCard支付与SDK悬浮窗初始化冲突问题。
### Version：4.3.23
修复港台发行区MyCard支付与Facebook的SDK初始化冲突问题。
### Version：4.3.22
1. 修改韩国发行区所使用的IGAWorks统计SDK的Deep Link配置，并去掉游戏主Activity的launchMode="singleTask"的设置；
2. 修复已知bug。
### Version：4.3.16
优化逻辑代码。
### Version：4.3.9
解决SDK初始化时的bug（需同时更换so库文件）。
### Version：4.3.7
解决SDK初始化成功后的回调bug问题。
### Version：4.3.5
1. 优化SDK初始化逻辑；
2. 增加AGPManager.eglsExit()游戏退出接口（必接接口）；
3. 更新韩国发行区内部统计SDK（IGAWorks）版本至4.6.0（请留意对接文档中，游戏工程及AGP相关的Gradle配置）；
4. 韩国发行区的游戏，其游戏启动Activity的“launchMode”属性必须为“singleTask”。
### Version：4.3.1
1. 解决SDK初始化异常问题；
2. AGS增加库引用：api 'com.android.support.constraint:constraint-layout:1.0.2'。
### Version：4.3.0
优化网络通信接口及其他部分业务逻辑，在更新SDK时请修改版本号后再同步至最新版本，并且需要更换so文件。
### Version: 4.2.18
1. 优化逻辑代码；
2. 使用最新语法修改gradle脚本中的库引用部分。
### Version: 4.2.14
将以下sdk中的基础库上传至Maven仓库，在对接时，请留意文档中相关部分的使用方法修改：
<br />egls-agp-sdk.aar
<br />egls-ags-sdk.aar
<br />egls-android-support.aar
### Version: 4.2.11
完善4.2.10版本。
### Version: 4.2.10
修复韩国当地部分机型在读取大容量文字时引发的系统接口报错问题。
### Version: 4.2.9
部分逻辑代码优化。<br /><br />
### Version: 4.2.8
1. 修复Facebook登录无响应问题；
2. 增加Appsflyer的devKey配置，如果有特殊需求，可以在Manifest文件中添加meta标签，其name为“CHANNEL_AF_DEV_KEY”。<br /><br />
### Version: 4.2.7
1. 优化网络交互机制；
2. 修改接口AGPManager.onDestroy()的接口名拼写错误；
3. 将AGP、AGS中的so文件从aar中独立出来，便于在SDK对接时对so文件类型的选择。<br /><br />
### Version: 4.2.6
1. 修改消息提示面板UI；
2. 在用户中心页面增加SDK版本号的显示。<br /><br />
### Version: 4.2.5
1. 去掉在中国大陆发行的游戏对Google、Facebook的库依赖；
2. 简化Facebook登录逻辑代码；
3. 更新了AppsFlyer的SDK，并请更改引入的配置。<br /><br />
### Version: 4.2.4
修复部分发行区错误引用AppsFlyer库的问题。<br /><br />
### Version: 4.2.3
1. 修复4.2.0版本中在进行自动登录时引起的闪退问题；
2. 优化google支付流程；
3. 增加EGLS账号记忆功能，在切换账号时，点击EGLS的图标，弹出已登录EGLS账号的列表供玩家选择；
4. 完善登录流程；
5. CN发行区增加QQ登录。<br /><br />
### Version: 4.2.2
修复4.2.0版本中在游戏必要权限申请的过程中选择拒绝后闪退的问题。<br /><br />
### Version: 4.2.1
1. 修复Google登录时无法取消的问题；
2. 修复悬浮窗在安卓8.0系统的权限提示错误问题；
3. 修复4.2.0版本中注册账号闪退的问题。<br /><br />
### Version: 4.2.0
1. AGP、AGS的核心库及资源等已都打包成“aar”文件，在升级至4.2.0前，请先删除原有的Module然后重新导入；
2. 增加登录banner信息提示，并在banner中添加Egls账号的切换按钮（banner3秒后自动消失，之后响应登录回调）；
3. 优化部分逻辑代码。<br /><br />
### Version: 4.1.7
1. 将AGS的AndroidManifest.xml文件中的AGSShareActivity配置移除，需在游戏项目中的AndroidManifest.xml文件中添加该配置；
2. 优化部分逻辑代码。<br /><br />
### Version: 4.1.6
1. 删除旧版Facebook相关的资源和代码，引用最新版Facebook功能；
2. minSdkVersion升至为16，compileSdkVersion请用26。<br /><br />
### Version: 4.1.5
1. 修改权限弹窗提示功能，即：在首次运行时，当targetSdkVersion>=23且deviceSdkVersion>=23时，才会弹出；
2. 添加“AGPManager.addPermissionContent()”接口；
3. 修复台湾发行区游戏在支付时引起的缺失jar异常；
4. 修改sdk的后台服务设置。<br /><br />
### Version: 4.1.4
修复Facebook分享异常问题。<br /><br />
### Version: 4.1.3
修复IgawHelper类中的接口被误混淆的问题。<br /><br />
### Version: 4.1.2
1. 创立SDK的Android Studio版本；
2. 修复4.1.1版本中闪退的bug；
3. 优化游戏必要权限检测逻辑，提供addNecessaryPermission()接口；
4. 为适应Android Studio项目工程中Gradle的productFlavor配置，提供addFlavorsBasePackage()接口。<br /><br />
