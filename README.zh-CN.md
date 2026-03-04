[English](README.md) | 简体中文

# TUIKit Flutter

TUIKit Flutter 是腾讯云推出的一套 Flutter UI 组件套件，涵盖**即时通讯**、**音视频通话**、**互动直播**、**多人音视频会议**等场景，帮助开发者快速在 App 中集成实时通讯能力。

> **关于表情版权说明：**
> 出于对表情设计版权的尊重，本项目不包含大表情元素的切图。商业上线前，请替换为您自己设计或拥有版权的表情包。默认的小黄脸表情包版权归腾讯云所有，如需获得授权，请[联系我们](https://trtc.io/contact)。
>
> <img src="https://qcloudimg.tencent-cloud.cn/image/document/6438e8feb7bba909511e0d798dfaf91d.png" width="300px" />

---

## 组件列表

| 组件 | 路径 | pub 包名 | 版本 | 说明 |
|------|------|---------|------|------|
| **TUIKit (IM)** | `chat/uikit/` | — | — | 即时通讯 UI 组件库（消息、会话、联系人） |
| **TUICallKit** | `call/` | `tencent_calls_uikit` | 4.0.6 | 1v1 与群组音视频通话 |
| **TUILiveKit** | `live/livekit/` | `tencent_live_uikit` | 3.6.4 | 互动直播（主播推流、观众观看、连麦） |
| **弹幕组件** | `live/live_uikit_barrage/` | `live_uikit_barrage` | 2.0.0 | 直播弹幕 |
| **礼物组件** | `live/live_uikit_gift/` | `live_uikit_gift` | 3.0.0 | 直播礼物特效 |
| **TUIRoomKit** | `room/` | `tencent_conference_uikit` | 4.0.0 | 多人音视频会议（企业会议、在线课堂） |
| **atomic-x** | `atomic-x/` | `tuikit_atomic_x` | 3.6.6 | 底层原子 UI 组件库（被各模块共同依赖） |
| **Demo App** | `application/` | — | — | 集成所有模块的综合演示应用 |

---

## 环境要求

| 平台 | 版本要求 |
|------|---------|
| Flutter SDK | ≥ 3.27.4 |
| Dart SDK | ≥ 3.4.0, < 4.0.0 |
| Android | minSdkVersion 21（Android 5.0+） |
| iOS | 12.0+ |

---

## 快速开始（运行 Chat Demo）

### 第一步：创建应用

1. 登录 [腾讯云即时通信控制台](https://console.trtc.io/)，若已有应用请记录其 SDKAppID。
2. 在**应用列表**页面点击**创建应用**。
3. 填写应用信息后点击**确认**，系统自动生成 **SDKAppID**，请记录备用。

### 第二步：获取密钥

1. 在应用列表中，点击目标应用行的**应用配置**，进入应用详情页。
2. 点击**查看密钥**，复制并妥善保存密钥信息。

> **请勿泄露密钥，避免造成腾讯云流量损失。**

### 第三步：配置源码

1. 克隆本项目：
   ```bash
   git clone https://github.com/Tencent-RTC/TUIKit_Flutter.git
   ```
2. 打开 `chat/demo/lib/login_page.dart`，填入以下参数：
   - `SDKAPPID`：替换为第一步获取的 SDKAppID
   - `SECRETKEY`：替换为第二步获取的密钥

<img src="https://sdk-im-1252463788.cos.ap-hongkong.myqcloud.com/tools/resource/chat/SDKAppID_SecretKey_Flutter.png" width="800"/>

> **安全提示：** 在客户端代码中配置 SECRETKEY 存在密钥泄露风险，仅适用于本地运行 Demo 和功能调试。
> 正确的 UserSig 下发方式是将计算逻辑集成到您的服务端，由服务端 API 实时生成 UserSig 并下发给 App。详情参见[服务端计算 UserSig](https://trtc.io/document/34385?product=chat&menulabel=serverapis)。

### 第四步：编译运行

1. 用 Android Studio 打开 `TUIKit_Flutter/chat/demo`。
2. 执行依赖安装：
   ```bash
   flutter pub get
   ```
3. 连接 Android/iOS 真机或启动模拟器，运行：
   ```bash
   flutter run
   ```

运行成功后界面如下：

<table border="1" bordercolor="#eeeeee" style="border-collapse: collapse;">
  <tr>
    <td align="center" style="padding: 5px;">
      <img src="https://github.com/user-attachments/assets/8027b70b-97f7-4759-88b1-86d422ebe9ae" width="300"/>
    </td>
  </tr>
</table>

---

## 各模块文档

- [TUICallKit — 音视频通话](call/README.md)
- [TUILiveKit — 互动直播](live/livekit/README.md)
- [TUIRoomKit — 多人会议](room/README.zh-CN.md)

---

## 许可证

本项目基于 [MIT License](LICENSE) 开源。

## 联系与支持

- 官方文档：[腾讯云实时音视频](https://cloud.tencent.com/product/trtc)
- 问题反馈：[GitHub Issues](https://github.com/Tencent-RTC/TUIKit_Flutter/issues)
- 技术支持：<info_rtc@tencent.com>
