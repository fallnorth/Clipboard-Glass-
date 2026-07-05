**中文版**

Clipboard Glass 是一款为 Windows 打造的轻量剪贴板历史管理工具，以液态玻璃视觉语言构建，在桌面之上呈现半透明、圆润、有呼吸感的悬浮面板，将每一次复制操作沉淀为可回溯的轻量记忆。

打开应用，你会看到一张温润的玻璃卡片悬浮在屏幕中央。左上角标注着 Clipboard 与 history，右侧一列圆形按钮依次排开：搜索、展开历史、一键清空、置顶切换、折叠收拢和关闭。两个视觉模式——透明与磨砂——置于顶部中央，点击即可平滑过渡，色彩和玻璃参数在两种风格间连续渐变，切换无跳动，界面结构始终保持统一。

透明模式下，面板由多层径向渐变和动态高光叠加而成，光标移入时会产生柔和的光斑跟随效果，仿佛玻璃下方有光源在流动。磨砂模式下，面板切换为浅灰白基调，降低视觉干扰，适合长时间办公时使用。

搜索功能被设计成一体式变形控件。收起时是一枚圆形放大镜图标，点击后展开为圆角长条搜索栏，放大镜自身随之淡入输入框左侧，形成一个连续的生长动画。输入关键词即可实时过滤历史记录，点击面板其他位置或空白处，搜索栏自动收拢还原。

历史记录区域支持两种视图。默认显示最近三条记录，点击展开图标可切换到完整历史视图，列表可滚动浏览，最多保留 60 条。滚动区域的顶部和底部应用了渐变遮罩，超出可视范围的内容自然淡出，避免了生硬的裁切边界。每条历史记录显示为独立的玻璃卡片，预览文字采用单行省略，下方标注记录时间。单击卡片即复制该条内容至系统剪贴板，右击则弹出上下文菜单，支持单独删除。

一键清空按钮位于工具栏中，点击即清除全部历史数据，同时将变更写入本地持久化文件，确保状态一致。应用的数据存储路径为 `%LocalAppData%\ClipboardGlass\history.json`，每次复制、删除或清空操作都会触发自动保存，重启后历史完整复原。

面板本身可折叠。点击折叠按钮后，下半部分的历史列表区域以与玻璃面板相同的缓动曲线淡出并收缩至零高度，面板整体缩减为一条仅含标题与工具栏的轻量横条，宽度不变，高度降至 76 像素，再次点击即可展开复原。折叠和展开过程中，所有可见元素的运动节奏统一，不存在突兀的跳变或闪烁。

窗口始终置顶，可随时通过置顶按钮关闭该行为。整个窗口支持拖拽，拖拽区域覆盖标题栏以下的玻璃表面，光标变为移动状态，符合 Windows 原生窗口操作习惯。

性能方面，透明模式下玻璃模糊效果由 WebView2 的 backdrop-filter 实现，GPU 加速渲染，空闲时 CPU 占用接近零。磨砂模式进一步降低了模糊强度，适合在笔记本电池模式下长时间运行。应用体积轻量，单一可执行文件配合 WebView2 运行库即可启动，无需额外安装依赖。

Clipboard Glass 的定位不是重型剪贴板管理器，而是一块安静悬浮在桌面上的玻璃便签，不抢注意力，不占空间，在你需要时出现，在你不需要时隐去。它以克制的功能集和精细的动效打磨，让复制与回找这一高频操作变得流畅、自然且愉悦。

---

**English Version**

Clipboard Glass is a lightweight clipboard history utility for Windows, wrapped in a liquid-glass visual language. It floats a translucent, soft-edged panel above the desktop, turning every copy action into a quietly retrievable memory.

At launch, a rounded glass card settles near the center of the screen. The top-left bears the label Clipboard and its subtitle history. To the right, a row of circular icon buttons gives quick access to search, history expansion, clear-all, topmost toggle, collapse, and close. Two visual modes — transparent and frosted — sit at the top center as a pill-shaped switcher. Tapping between them triggers a smooth CSS-backed transition: the glass parameters shift, the panel background gradients cross-fade, and the overall tone moves from cool blue-white translucency to a calm gray-white matte finish — all without a single DOM rebuild.

In transparent mode, the panel is layered with radial gradients and a dynamic highlight that follows the cursor, creating the illusion of a light source sliding beneath the glass. In frosted mode, the surface settles into a quieter gray-white backdrop, reducing visual noise for extended work sessions.

The search experience is built as a single morphing control. Collapsed, it is a circular magnifying-glass button. Tap it, and the button expands in width, the glass icon slides to the left edge of an emerging rounded input field, and the text cursor pulses into place — one continuous animation. Type to filter the clipboard history in real time. Click anywhere else on the panel or the background, and the search bar retracts back into the circular icon.

The history list offers two views. By default, the three most recent entries are visible. Click the history button to reveal the full scrollable list, capped at 60 entries. The scroll region applies gradient masks at the top and bottom edges, so overflowing content fades gracefully instead of cutting off abruptly. Each entry appears inside its own glass card: a single-line preview with ellipsis and a timestamp below. Left-click copies that entry to the system clipboard instantly. Right-click opens a context menu with a delete option, letting you prune individual items.

A single trash button in the toolbar erases the entire history in one tap. The change is immediately written to the local persistence file at `%LocalAppData%\ClipboardGlass\history.json`. Every copy, deletion, or bulk clear triggers an automatic save. Close and reopen the app, and your history is exactly where you left it.

The panel is collapsible. Press the collapse button, and the lower list region fades and shrinks to zero height using the same easing curve as the glass panel itself, reducing the window to a slim 76-pixel toolbar while maintaining its full width. Press again, and it re-expands seamlessly. No snapping, no jarring jumps — one unified motion.

The window stays always-on-top by default, toggleable via the pin button. The entire glass surface from the title area upward acts as a drag handle, matching the behavior of a native Windows window.

On the performance side, the transparent mode relies on GPU-accelerated backdrop-filter through WebView2, drawing minimal CPU at idle. The frosted mode reduces blur intensity further for longer battery-friendly sessions. The application ships as a single portable executable alongside the required WebView2 runtime DLLs — no installer, no external dependencies, unpack and run.

Clipboard Glass is not a heavy clipboard manager. It is a small glass note hovering at the edge of your workspace, showing up when you need it, fading back when you do not. Its restrained feature set and carefully tuned motion make the high-frequency act of copying and revisiting feel fluid, natural, and quietly satisfying.
