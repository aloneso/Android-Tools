# Android-Tools


#### apktool
这里是apktool官网地址：https://ibotpeaches.github.io/Apktool/
##### 1. 解压
```
java -jar apktool_2.4.0.jar d POC-release.apk  -o dir
```
##### 2. 重新打包
```
 java -jar apktool_2.4.0.jar b dir/ -o test.apk
```

#### dex2jar
这里是apktool官网地址：

https://sourceforge.net/projects/dex2jar/

```
d2j-dex2jar.bat app-debug.apk -o app-debug.jar

```

#### jadx

直接查看资源与代码

#### enjarify

将apk反编译成java源码
enjarify *.apk -o out.jar


#### Auto-Sign

 给重新打包的apk签名

```
java -jar signapk.jar testkey.x509.pem testkey.pk8 test.apk test_signed.apk
```

#### keytool-importkeypair
把Android平台的签名文件转换成apk签名的keystore

```
keytool-importkeypair -k ~/.android/debug.keystore -p android -pk8 platform.pk8 -cert platform.x509.pem -alias platform
```