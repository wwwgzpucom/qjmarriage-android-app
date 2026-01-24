# 齐家婚姻相亲 Android App

基于 WebView 的齐家婚姻相亲网站 Android 客户端应用。

## 项目简介

这是一个将 [齐家婚姻相亲网站](https://qjmarriage.com/) 封装为原生 Android 应用的项目，使用 Smart WebView 框架构建。

## 功能特性

- ✅ 加载齐家婚姻相亲网站 (https://qjmarriage.com/)
- ✅ 下拉刷新
- ✅ 文件上传（支持相机和相册）
- ✅ 地理位置权限
- ✅ 推送通知
- ✅ 离线提示
- ✅ 网络错误处理
- ✅ 返回键网页后退

## 技术栈

- **语言**: Java
- **最低 SDK**: Android 7.0 (API 24)
- **目标 SDK**: Android 14 (API 36)
- **构建工具**: Gradle 8.14
- **AGP 版本**: 8.7.3
- **Java 版本**: 17

## 项目信息

- **包名**: `com.qjmarriage.app`
- **版本**: 1.0.0
- **版本号**: 1

## 构建说明

### 环境要求

- Android Studio Ladybug 或更高版本
- JDK 17
- Android SDK 36

### 编译步骤

1. 克隆项目
```bash
git clone https://github.com/wwwgzpucom/qjmarriage-android-app.git
cd qjmarriage-android-app
```

2. 使用 Android Studio 打开项目

3. 同步 Gradle
```bash
./gradlew build
```

4. 生成 APK
```bash
./gradlew assembleDebug    # Debug 版本
./gradlew assembleRelease  # Release 版本
```

### 输出文件

- Debug APK: `app/build/outputs/apk/debug/app-debug.apk`
- Release APK: `app/build/outputs/apk/release/app-release-unsigned.apk`

## 配置说明

主要配置文件位于 `app/src/main/assets/swv.properties`，可以修改：

- `app.url` - 网站地址
- `build.application.id` - 应用包名
- `build.version.code` - 版本号
- `build.version.name` - 版本名称
- `feature.pull.refresh` - 是否启用下拉刷新
- 更多配置请查看配置文件注释

## 上架准备

### 签名 APK

1. 生成签名密钥
```bash
keytool -genkey -v -keystore qjmarriage.jks -keyalg RSA -keysize 2048 -validity 10000 -alias qjmarriage
```

2. 在 `app/build.gradle` 中配置签名信息

3. 构建签名版本
```bash
./gradlew assembleRelease
```

### 应用市场要求

- ✅ 应用图标（已包含）
- ✅ 启动页（已包含）
- ⚠️ 隐私政策（需要添加）
- ⚠️ 用户协议（需要添加）
- ⚠️ 软著和 ICP 备案
- ⚠️ 网络文化经营许可证（婚恋类应用）

## 许可证

本项目基于 [Smart WebView](https://github.com/mgks/Android-SmartWebView) 构建，遵循 MIT 许可证。

## 联系方式

- 网站：https://qjmarriage.com/
- GitHub：https://github.com/wwwgzpucom/qjmarriage-android-app

## 更新日志

### v1.0.0 (2026-01-25)
- 初始版本发布
- 集成齐家婚姻相亲网站
- 支持基础 WebView 功能
- 启用下拉刷新
