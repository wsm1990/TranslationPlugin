
TranslationPlugin
=================

[![Jetbrains Plugins][plugin-img]][plugin]
[![License][license-img]][license]
[![Build Status][build-img-master]][travis-ci]
[![GitHub release][release-img]][latest-release]
[![Version][version-img]][plugin]
[![Downloads][downloads-img]][plugin]
[![Financial Contributors on Open Collective][open-collective-badge]][open-collective]

### JetBrains IDE/Android Studio 翻译插件

![screenshots](./images/screenshots.gif)

特征
----
- 多翻译引擎
  - Google翻译
  - 有道翻译
  - 百度翻译
- 多语言互译
- 语音朗读
- 自动选词
- 自动单词拆分
- 单词本

支持的 **Jetbrains IDE** 产品:
- Android Studio
- AppCode
- CLion
- DataGrip
- GoLand
- IntelliJ IDEA Ultimate
- IntelliJ IDEA Community
- IntelliJ IDEA Educational
- MPS
- PhpStorm
- PyCharm Professional
- PyCharm Community
- PyCharm Educational
- Rider
- RubyMine
- WebStorm

安装
----
- **使用 IDE 内置插件系统安装:**
  - <kbd>Preferences(Settings)</kbd> > <kbd>Plugins</kbd> > <kbd>Browse repositories...</kbd> > <kbd>搜索并找到"Translation"</kbd> > <kbd>Install Plugin</kbd>

- **手动安装:**
  - 下载[插件包][latest-release] -> <kbd>Preferences(Settings)</kbd> > <kbd>Plugins</kbd> > <kbd>Install plugin from disk...</kbd> -> 选择插件包并安装（无需解压）

重启**IDE**.

使用
----
1. **申请有道智云翻译服务（可选）:**
   - 注册[有道智云](http://ai.youdao.com)帐号并获取其**应用ID**和**应用密钥**
   - 绑定**应用ID**和**应用密钥**：<kbd>Preferences(Settings)</kbd> > <kbd>\[Other Settings]</kbd> > <kbd>Translation</kbd> > <kbd>有道翻译</kbd>

   注：请注意保管好你的**应用密钥**，防止其泄露。如帐号欠费，将无法使用。

2. **申请百度翻译服务（可选）:**
   - 注册[百度翻译开放平台](http://api.fanyi.baidu.com/api/trans/product/desktop?req=developer)帐号并获取其**应用ID**和**应用密钥**
   - 绑定**应用ID**和**应用密钥**：<kbd>Preferences(Settings)</kbd> > <kbd>\[Other Settings]</kbd> > <kbd>Translation</kbd> > <kbd>百度翻译</kbd>

   注：请注意保管好你的**应用密钥**，防止其泄露。如帐号欠费，将无法使用。

3. **开始翻译:**

   <kbd>选择文本或者鼠标指向文本</kbd> > <kbd>单击鼠标右键</kbd> > <kbd>Translate</kbd>

   或者使用快捷键进行翻译，详见 **[Actions](#actions)**

4. **翻译并替换:**

   翻译目标文本并将其替换。当翻译目标语言为英文时，会分别输出为**骆驼式输出**、**含单词分隔符输出**（输出包含多个单词时，分隔符可在插件配置页面中配置：翻译设置 > 分隔符）和**原输出**。

   用法：<kbd>选择文本或者鼠标指向文本</kbd> > <kbd>单击鼠标右键</kbd> > <kbd>Translate and Replace...</kbd>（或者使用快捷键进行翻译，详见 **[Actions](#actions)**）。

5. **切换翻译引擎:**

   点击状态栏的翻译引擎状态图标或者使用快捷键 <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd>（Mac OS: <kbd>Control</kbd> + <kbd>Meta</kbd> + <kbd>Y</kbd>）可以快速切换翻译引擎，目前有谷歌翻译、有道翻译和百度翻译。


插件配置
------

![settings](./images/settings.png)


Actions
-------
- **Show Translation Dialog...**

  打开翻译对话框。默认显示在工具栏上。默认快捷键:

  - Windows - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>O</kbd>
  - Mac OS - <kbd>Control</kbd> + <kbd>Meta</kbd> + <kbd>I</kbd>

- **Translate**

  取词并翻译。如果有已选择的文本，优先从选择的文本内取词，否则默认以最大范围自动取词（该取词模式可在Settings中配置）。默认显示在编辑器右键菜单上，默认快捷键:

  - Windows - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Y</kbd>
  - Mac OS - <kbd>Control</kbd> + <kbd>Meta</kbd> + <kbd>U</kbd>

- **Translate(Inclusive)**

  取词并翻译。自动以最大范围取最近的所有词，忽略手动选择的文本。默认快捷键: (无)

- **Translate(Exclusive)**

  取词并翻译。自动取最近的单个词，忽略手动选择的文本。默认快捷键: (无)

- **Translate and Replace...**

  翻译并替换。取词方式同`Translate`操作。默认显示在编辑器右键菜单上，默认快捷键:

  - Windows - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd>
  - Mac OS - <kbd>Control</kbd> + <kbd>Meta</kbd> + <kbd>O</kbd>

- **Translate Text Component**

  翻译一些文本组件（如快速文档、提示气泡、输入框……）中选中的文本，不支持自动取词。默认快捷键:

  - Windows - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Y</kbd>
  - Mac OS - <kbd>Control</kbd> + <kbd>Meta</kbd> + <kbd>U</kbd>

- **Choose Translator**

  快速切换翻译引擎。默认快捷键:

  - Windows - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd>
  - Mac OS - <kbd>Control</kbd> + <kbd>Meta</kbd> + <kbd>Y</kbd>

- **Show Instant Translation Dialog**

  显示即时翻译对话框。默认快捷键: (无)

- **Word of the Day**

  显示每日单词对话框。默认快捷键: (无)

FAQ
---
1. **出现网络错误或者网络连接超时怎么办？**

   **答**：  
   - 检查网络环境，确保网络畅通。
   - 检查是否是因为使用了代理软件而导致插件无法访问翻译API。
   - 检查IDE代理配置，查看是否是因为IDE代理配置导致的问题。
   - 如果使用的是谷歌翻译，检查谷歌翻译配置，查看是否勾选了`使用translate.google.com`选项（如果系统语言环境是非中文的话，此选项是默认勾选的），translate.google.com在国内是需要VPN才能访问的。另外，TTS功能使用的也是谷歌翻译的API。

2. **翻译内容出现乱码怎么办？**

   **答**：出现乱码一般是因为字体中没有相应的字符的问题，可以到插件的设置页面修改字体以解决乱码问题（如下图所示）。
   
   ![screenshots](./images/settings_font.png)

3. **无法保存应用密钥怎么办?**

   **答**：可以尝试将密码保存方式改成`In KeePass`方式 (<kbd>Settings</kbd> > <kbd>Appearance & Behavior</kbd> > <kbd>System Settings</kbd> > <kbd>Passwords</kbd>)，原因与细节：
   - MacOS，请另阅 [#81](https://github.com/YiiGuxing/TranslationPlugin/issues/81)
   - Linux，请另阅 [#115](https://github.com/YiiGuxing/TranslationPlugin/issues/115)

4. **快捷键不能使用怎么办？**

   **答**：快捷键不能使用可能是因为被其他插件或者外部应用占用了，可以为相应的操作重新设置新的快捷键。

更新日志
--------
## [v2.5.1](https://github.com/YiiGuxing/TranslationPlugin/tree/v2.5.1) (2019-11-01)

- 修复了导致在Android Studio上崩溃的一个致命错误
- 修复了忽略内容在一些特定的情况下会失效的问题
- 修复了重复显示每日单词对话框会导致界面异常的问题
- 一些功能增强与优化

[完整的更新历史记录](./CHANGELOG.md)


Support
-------

您可以通过执行以下任意操作来贡献和支持此项目：
* 在GitHub上标星
* 将插件分享给您的朋友/同事
* 提交PR
* 反馈问题
* 提出您的想法/建议
* 如果您喜欢这个插件，请考虑捐赠以维持插件的相关活动：

  <table>
    <thead align="center">
      <tr>
        <th>Open Collective</th>
        <th>支付宝</th>
        <th>微信支付</th>
      </tr>
    </thead>
    <tr align="center">
      <td>
        <a href="https://opencollective.com/translation-plugin" target="_blank">
            <img src="./images/open_collective.png">
        </a>
      </td>
      <td><img src="./images/alipay.png"></td>
      <td><img src="./images/wechat.png"></td>
    </tr>
  </table>

感谢您的支持！

其他插件
------

- [FIGlet](https://github.com/YiiGuxing/intellij-figlet)
- [Material Design Color Palette](https://github.com/YiiGuxing/material-design-color-palette)


[build-img-dev]: https://img.shields.io/travis/YiiGuxing/TranslationPlugin/dev.svg?style=flat-square
[build-img-master]: https://img.shields.io/travis/YiiGuxing/TranslationPlugin/master.svg?style=flat-square
[license-img]: https://img.shields.io/github/license/YiiGuxing/TranslationPlugin.svg?style=flat-square
[release-img]: https://img.shields.io/github/release/YiiGuxing/TranslationPlugin.svg?style=flat-square
[plugin-img]: https://img.shields.io/badge/JetBrainsPlugin-8579-orange.svg?style=flat-square
[downloads-img]: https://img.shields.io/jetbrains/plugin/d/8579.svg?style=flat-square
[version-img]: https://img.shields.io/jetbrains/plugin/v/8579.svg?style=flat-square&colorB=0091ea
[latest-release]: https://github.com/YiiGuxing/TranslationPlugin/releases/latest
[license]: https://github.com/YiiGuxing/TranslationPlugin/blob/master/LICENSE
[travis-ci]: https://travis-ci.org/YiiGuxing/TranslationPlugin
[plugin]: https://plugins.jetbrains.com/plugin/8579
[open-collective]: https://opencollective.com/translation-plugin
[open-collective-badge]: https://opencollective.com/translation-plugin/all/badge.svg?label=financial+contributors&style=flat-square&&color=D05CE3

## Contributors

### Code Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/YiiGuxing/TranslationPlugin/graphs/contributors"><img src="https://opencollective.com/translation-plugin/contributors.svg?width=890&button=false" /></a>

### Financial Contributors

Become a financial contributor and help us sustain our community. [[Contribute](https://opencollective.com/translation-plugin/contribute)]

#### Individuals

<a href="https://opencollective.com/translation-plugin"><img src="https://opencollective.com/translation-plugin/individuals.svg?width=890"></a>

#### Organizations

Support this project with your organization. Your logo will show up here with a link to your website. [[Contribute](https://opencollective.com/translation-plugin/contribute)]

<a href="https://opencollective.com/translation-plugin/organization/0/website"><img src="https://opencollective.com/translation-plugin/organization/0/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/1/website"><img src="https://opencollective.com/translation-plugin/organization/1/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/2/website"><img src="https://opencollective.com/translation-plugin/organization/2/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/3/website"><img src="https://opencollective.com/translation-plugin/organization/3/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/4/website"><img src="https://opencollective.com/translation-plugin/organization/4/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/5/website"><img src="https://opencollective.com/translation-plugin/organization/5/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/6/website"><img src="https://opencollective.com/translation-plugin/organization/6/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/7/website"><img src="https://opencollective.com/translation-plugin/organization/7/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/8/website"><img src="https://opencollective.com/translation-plugin/organization/8/avatar.svg"></a>
<a href="https://opencollective.com/translation-plugin/organization/9/website"><img src="https://opencollective.com/translation-plugin/organization/9/avatar.svg"></a>
