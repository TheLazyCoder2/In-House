# iOS企业应用的分发的分发步骤:

1.使用企业证书打包的IPA，推荐使用itunes打包方式，可以避免一些In-House时的一些坑；

2.配置plist文件，plist文件的必要条目为ipa下载链接（支持http协议）、应用包名称（Bundle ID）；

3.plist文件必须用https协议访问，就是说你的发起下载的网站必须支持https。如果你没有，有两种解决方式：一、百度搜索SSL证书，有一些可以免费使用SSL证书；二、使用GitHub的网址，最简单也是本次推荐的方式；

在GitHub上边要打开plist文件，选择Raw类型，然后复制页面链接即可：（例如：https://raw.githubusercontent.com/TheLazyCoder2/In-House/master/Info.plist）

4.随后使用itms-services协议进行访问就可以了安装应用了：（例如：itms-services://?action=download-manifest&url=https://raw.githubusercontent.com/TheLazyCoder2/In-House/master/Info.plist）


有任何问题可以联系我的QQ：32510112
