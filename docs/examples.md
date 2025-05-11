# 一些示例代码

MkDocs 文档使用 Python-Markdown 转换，并开启了一些（官方和第三方）拓展。



> [!NOTE]
>
> 提醒内容（Github风格）



测试

!!! note This is the admonition title
    This is the admonition body


> 单纯引用



??? info "pymdown details" 

    details 风格的

<details class="info">
<summary>Click me</summary>
  似乎折叠内容内部的格式只在GFM里生效。类似下面：
    ## 你好
</details>



<details class="tip">
<summary>使用HTML生成折叠</summary>
<p>
调整class的内容以生成不同的折叠框
</p>
</details>


!!! info "注意"

    该登录方式只适用于名称中带有 `desktop` 的虚拟机镜像，通常为 01 到 09 号镜像。

!!! success "浏览器支持"

    此登录方式需要浏览器支持。以下浏览器是受支持的：
    
    - :fontawesome-brands-chrome: Google Chrome 49 或以上
    - :fontawesome-brands-firefox-browser: Mozilla Firefox 44 或以上
    - :fontawesome-brands-safari: Safari 11 或以上
    - :fontawesome-brands-opera: Opera 36 或以上
    - :fontawesome-brands-edge: Microsoft Edge 79 或以上
    
    我们推荐最新版本的 [Microsoft Edge](https://www.microsoft.com/zh-cn/edge), [Google Chrome](https://www.google.cn/chrome/) 和 [Mozilla Firefox](https://www.mozilla.org/zh-CN/firefox/new/)，它们能提供最完整的功能和最好的使用体验。
    
    **请注意，我们不支持来历不明的杂牌浏览器**。如果你正在使用该类浏览器，并且发现无法使用远程桌面连接，请点击上面其中一个链接下载最新的浏览器。不仅仅在 Vlab 上——它们在几乎所有网站里都能提供相比于你的浏览器更好的使用体验、性能与安全性。
    
    由于技术原因，浏览器 VNC 登录与网络信息中心提供的 Web VPN 服务（wvpn.ustc.edu.cn）不兼容，尝试通过 Web VPN 登录会收到各种错误信息。请直接访问 [vlab.ustc.edu.cn](https://vlab.ustc.edu.cn/) 登录。

浏览器登录非常简单，只需要打开[虚拟机管理页面](https://vlab.ustc.edu.cn/vm/)，点击相应虚拟机的 \[桌面连接\] 按钮即可。

??? info "关闭 VNC 通知"

    使用 VNC 登录时会看到加入 QQ 群的通知，**我们会在该 QQ 群中发布如停机维护等重要通知**。
    
    若你想要选择关闭 VNC 通知，可以在 [此处](https://vlab.ustc.edu.cn/vm/notif) 设置。

## 使用组合键 {#combo-keys}

!!! tip "客户端更方便"

    [使用 Tiger 客户端](vnc.md#tigervnc)能够更方便地使用虚拟机的完整功能，因此如果你经常在虚拟机上进行复杂操作的话，我们建议你使用 TigerVNC 客户端。

在浏览器中使用组合键会受到一定限制，例如你的浏览器很可能会将 <kbd>Ctrl</kbd>+<kbd>W</kbd> 理解为“关闭当前标签”，或将 <kbd>Ctrl</kbd>+<kbd>T</kbd> 理解为“打开一个新标签”。为了能将这些组合键正确发送至虚拟机，你可以使用侧边栏提供的组合键功能，如图：

![noVNC Combo Keys](../images/novnc-combo-keys.png)

从上到下的 6 个按键分别为 ==Ctrl==, ==Alt==, ==Super==, ==Tab==, ==Esc== 和 ==Ctrl+Alt+Del== 组合键。点击它们中的一个或多个，再按键盘上的字母数字键，即可向虚拟机发送组合键。

## 使用剪贴板 {#clipboard}

### 使用自动剪贴板 {#auto-clipboard}

在 Google Chrome 及 Microsoft Edge 上可以使用自动剪贴板功能。第一次使用前请先在虚拟机内使用以下命令更新软件包：

```
sudo apt update && sudo apt upgrade
```

接着在管理页面点击 \[桌面连接\] 按钮后，浏览器将会请求剪贴板权限，请选择允许，之后客户端系统的剪贴板和虚拟机的剪贴板将会自动同步。
如果你不想使用自动剪贴板，可以打开左侧工具栏的设置，取消勾选 `Authomatic Clipboard` 后按以下方法使用手动剪贴板。

### 使用手动剪贴板 {#manual-clipboard}

如果你使用其他浏览器，如 Mozilla Firefox 或 Safari，由于技术限制自动剪贴板将不可用，请按以下方法使用手动剪贴板：

在虚拟机中复制文字后，点击展开左侧工具栏的第二个按钮即可查看虚拟机剪贴板中的内容。

![noVNC Clipboard Utility](../images/novnc-clipboard.png){: .img-border }

如果想从主机中复制文字进虚拟机，可以将文字粘贴进左侧工具栏弹出的文本框中，即可在虚拟机中粘贴。

## 左侧工具栏说明 {#novnc-toolbar}

左侧工具栏一共有 5 个按钮，如图：

![noVNC Toolbar](../images/novnc-toolbar.png)

从上往下功能依次为：

- [组合键](#combo-keys)
- [剪贴板](#clipboard)
- 全屏显示
- 设置
- 断开连接

## 桌面设置

关于一些常用的桌面设置，如

- 修改 VNC 分辨率
- 中文输入法

等，请参阅[桌面设置](vnc.md#desktop-settings)。