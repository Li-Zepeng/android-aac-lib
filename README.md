## 一、用途
* 学习多个mvvm框架后，去粗取精，全部使用当前日期最新的依赖库，对recyclerview.adapter，viewpagerAdater等进行了封装，一个类轻松实现多类型条目
* 本架构使用了google的AAC架构，基本采用kotlin语言开发，填了很多kotlin+mvvm的坑
* 没有使用rxjava（google自带的viewmodel完全可以替代此组件），anko等太激进的写法，适合公司项目稳定使用，便于java到kotlin的过渡
* 适合新项目直接依赖使用，老项目有依赖冲突可以下载去除多余依赖，其中common文件夹可以删除，为旧项目文件，因本人目前还有需要，暂时没有删除
* 使用这个库是为了多个项目使用同一基础组件，方便维护更新，提高开发效率
* demo还没有写好，还有一些业务层的封装经验，暂时没有上传
* 注意：目前因本人需要，依赖了常用的umeng，轮播，二维码，bug收集，okgo的封装，urls管理等本人精心封装好的组件，用不到的可以下载删除，替换
## 二、使用(version自行选择release中的最新版本)
* api 'com.github.Li-Zepeng:android_aac_lib:version'

## 三、包含依赖
* design库（包含v4，v7，v7-recyclerview，无cardview）

  "design"               : "com.android.support:design:$version.supportVersion",
* 约束性布局

  "constraint-layout"    : "com.android.support.constraint:constraint-layout:1.1.3",
* fragment页面框架库

  "navigation-ui"        : "android.arch.navigation:navigation-ui-ktx:$version.naviVersion",

  "navigation-fragment"  : "android.arch.navigation:navigation-fragment-ktx:$version.naviVersion",

* lifecycle

  "lifecycle-extensions" : "android.arch.lifecycle:extensions:$version.archVersion",
* kotlin https://kotlinlang.org/docs/reference/

  "kotlin"               : "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$version.kotlinVersion",

  "kotlin-reflect"       : "org.jetbrains.kotlin:kotlin-reflect:$version.kotlinVersion",
* 数据库（支持livedata）

  "room-runtime"         : "android.arch.persistence.room:runtime:$version.archVersion",

  "room-compiler"        : "android.arch.persistence.room:compiler:$version.archVersion",
* 分包库

  "multidex"             : "com.android.support:multidex:1.0.2",
* 状态栏 https://github.com/gyf-dev/ImmersionBar

  "statusbar"            : "com.gyf.immersionbar:immersionbar:2.3.2",
* 刷新 https://github.com/scwang90/SmartRefreshLayout

  "refreshLayout"        : "com.scwang.smartrefresh:SmartRefreshLayout:1.1.0-alpha-18",
* 底部导航 https://github.com/ittianyu/BottomNavigationViewEx

  "bottomNavigationView" : "com.github.ittianyu:BottomNavigationViewEx:2.0.2",
* 轮播（待优化：之后会自定义封装实现，便于转换androidx）https://github.com/youth5201314/banner

  "banner"               : "com.youth.banner:banner:1.4.10",
* json解析 https://github.com/google/gson

  "gson"                 : "com.google.code.gson:gson:2.8.5",
* 路由跳转库 https://github.com/alibaba/ARouter

  "arouter"              : "com.alibaba:arouter-api:1.4.1",
* 图片加载库 https://github.com/bumptech/glide  http://m.blog.csdn.net/sinyu890807/article/details/78582548

  "glide"                : "com.github.bumptech.glide:glide:4.8.0",
* 网路库 https://github.com/jeasonlzy/okhttp-OkGo

  "okgo"                 : "com.lzy.net:okgo:3.0.4",

  "okGoDown"             : "com.lzy.net:okserver:2.0.5",
* 友盟 https://www.umeng.com/

  "umeng_common"         : "com.umeng.umsdk:common:1.5.4",

  "umeng_utdid"          : "com.umeng.umsdk:utdid:1.1.5.3",

  "umengshare_sdk"       : "com.umeng.umsdk:share-core:6.9.4",

  "umengshare_shareboard": "com.umeng.umsdk:share-board:6.9.4",

  "umengshare_qq"        : "com.umeng.umsdk:share-qq:6.9.4",

  "umengshare_wechat"    : "com.umeng.umsdk:share-wx:6.9.4",

  "umengshare_sina"      : "com.umeng.umsdk:share-sina:6.9.4",

  "umengpush_sdk"        : "com.umeng.umsdk:push:5.0.2",
* 二维码

  "zxing"                : "com.google.zxing:core:3.3.0",
* 工具库 https://github.com/Blankj/AndroidUtilCode

  "utilcode"             : "com.blankj:utilcode:1.22.7",
* 腾讯bug收集 https://bugly.qq.com/docs/user-guide/instruction-manual-android/?v=20180521124306

  "bugly"                : "com.tencent.bugly:crashreport:latest.release",
* 网络、数据库抓包 http://facebook.github.io/stetho/  https://www.jianshu.com/p/03da9f91f41f

  "stetho"               : "com.facebook.stetho:stetho:latest.release",

  "stethoOkgo"           : "com.facebook.stetho:stetho-okhttp3:latest.release",
* 内存泄漏 https://github.com/square/leakcanary 为防止debug干扰，没有强制集成，可自行添加

  "leakcanary-release"   : "com.squareup.leakcanary:leakcanary-android-no-op:latest.release",

  "leakcanary-debug"     : "com.squareup.leakcanary:leakcanary-android:latest.release",