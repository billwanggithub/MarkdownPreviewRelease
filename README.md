# Markdown Preview

A lightweight Markdown editor with live preview for Windows, built with WPF (.NET 8) and MVVM architecture.

一款輕量級的 Markdown 編輯器，具有即時預覽功能，以 WPF（.NET 8）及 MVVM 架構打造，適用於 Windows。

![App Icon](Assets/app-256.png)

## Features / 功能特色

- **Side-by-side editing / 並排編輯** — AvalonEdit text editor with real-time WebView2 preview / AvalonEdit 文字編輯器搭配即時 WebView2 預覽
- **Syntax highlighting / 語法高亮** — Markdown-aware colorization in the editor (headings, bold, italic, code, links, blockquotes, lists) / 編輯器中的 Markdown 語法著色（標題、粗體、斜體、程式碼、連結、引用、清單）
- **Code block highlighting / 程式碼區塊高亮** — Highlight.js syntax highlighting in the preview with auto dark/light theme detection / 預覽中使用 Highlight.js 語法高亮，自動偵測亮色／暗色佈景主題
- **Copy code button / 複製程式碼按鈕** — Hover over any code block in the preview to copy its contents / 在預覽中懸停於程式碼區塊即可複製內容
- **Synchronized scrolling / 同步捲動** — Bidirectional scroll sync between editor and preview / 編輯器與預覽之間的雙向捲動同步
- **Light / Dark theme / 亮色／暗色佈景主題** — Toggle with Ctrl+T; applies to editor, preview, and UI / 使用 Ctrl+T 切換，套用至編輯器、預覽及介面
- **Export / 匯出** — Save rendered output as HTML or PDF with progress indicator and option to open the exported file / 將渲染結果儲存為 HTML 或 PDF，附進度指示與開啟檔案選項
- **Alert blocks / 提示區塊** — Insert GitHub-compatible alerts (Note, Tip, Important, Warning, Caution) with Ctrl+Shift+C / 使用 Ctrl+Shift+C 插入相容 GitHub 的提示區塊（備註、提示、重要、警告、注意）
- **Table insertion / 表格插入** — Insert Markdown tables with configurable rows and columns via Ctrl+Shift+T; formatting and CSV conversion are CJK-aware for correct column alignment / 使用 Ctrl+Shift+T 插入可設定列數與欄數的 Markdown 表格；格式化與 CSV 轉換支援 CJK 字元寬度計算，確保欄位正確對齊
- **Table of Contents / 目錄** — Insert a Markdown TOC from headings (Ctrl+Shift+O), or toggle an auto-generated TOC in the preview (Ctrl+Shift+D) / 從標題插入 Markdown 目錄（Ctrl+Shift+O），或在預覽中切換自動產生的目錄（Ctrl+Shift+D）
- **KaTeX math rendering / KaTeX 數學公式渲染** — Inline `$...$` and display `$$...$$` math expressions / 行內 `$...$` 與區塊 `$$...$$` 數學運算式
- **Mermaid diagrams / Mermaid 圖表** — Render flowcharts, sequence diagrams, and more from `mermaid` fenced code blocks / 從 `mermaid` 程式碼區塊渲染流程圖、時序圖等
- **Emoji support / 表情符號支援** — Render emoji shortcodes like `:smile:` in the preview / 在預覽中渲染表情符號簡碼（如 `:smile:`）
- **Footnotes / 腳註** — Support for Markdown footnotes with styled rendering / 支援 Markdown 腳註並附帶樣式渲染
- **Task lists / 任務清單** — Render `- [x]` / `- [ ]` checkboxes with proper styling / 渲染 `- [x]` / `- [ ]` 核取方塊並附帶正確樣式
- **Find / Replace / 尋找／取代** — Ctrl+F search panel with match case, whole word, regex options and current match position display; Ctrl+H opens replace mode with Replace and Replace All / Ctrl+F 搜尋面板支援區分大小寫、全字匹配、正規表示式及目前匹配位置顯示；Ctrl+H 開啟取代模式，支援取代與全部取代
- **Recent files / 最近的檔案** — Quick access to recently opened/saved files from the File menu / 從檔案選單快速存取最近開啟／儲存的檔案
- **Auto-save / 自動儲存** — Automatic draft saving every 30 seconds with crash recovery on next launch / 每 30 秒自動儲存草稿，下次啟動時可復原
- **Formatting toolbar / 格式工具列** — One-click buttons for Bold, Italic, Strikethrough, Blockquote, Inline Code, Code Fence, Bullet/Numbered/Task List, Insert Alert/Image/Table/TOC/Emoji, CSV⇄Table toggle, Force Refresh; plus toggles for Preview Only, TOC, Sync Scroll, Dark Mode, font pickers, and a language selector / 一鍵按鈕支援粗體、斜體、刪除線、引用、行內程式碼、程式碼區塊、項目符號／編號／任務列表、插入提示區塊／圖片／表格／目錄／表情符號、CSV⇄表格轉換、強制重新整理；另有僅預覽、目錄、同步捲動、暗色模式切換、字型選擇器及語言選擇器
- **Preview-only mode / 僅預覽模式** — Hide the editor and view rendered output full-width with Ctrl+M / 使用 Ctrl+M 隱藏編輯器，全寬檢視渲染結果
- **Multi-language UI / 多語系介面** — English and Traditional Chinese (繁體中文) with live switching via View > Language menu or the toolbar language selector / 英文與繁體中文，透過 檢視 > 語言 選單或工具列語言選擇器即時切換
- **Drag & drop / 拖放檔案** — Drop `.md`, `.markdown`, or `.txt` files to open / 拖放 `.md`、`.markdown` 或 `.txt` 檔案即可開啟
- **File association / 檔案關聯** — Register as the default viewer for `.md` / `.markdown` files / 註冊為 `.md` / `.markdown` 檔案的預設檢視器
- **Zoom control / 縮放控制** — Adjust editor and preview size with Ctrl+=/Ctrl+-/Ctrl+0 or Ctrl+Scroll / 使用 Ctrl+=/Ctrl+-/Ctrl+0 或 Ctrl+滾輪 調整編輯器與預覽大小
- **Incremental preview rendering / 增量預覽渲染** — Text edits update the preview via fast DOM swap instead of full page reload, eliminating flicker and preserving scroll position / 文字編輯透過快速 DOM 替換更新預覽，取代完整頁面重新載入，消除閃爍並保留捲動位置
- **Emoji picker & autocomplete / 表情符號選擇器與自動完成** — Insert emoji via picker dialog (Ctrl+Shift+E) or type `:` to trigger inline autocomplete / 透過選擇器對話框（Ctrl+Shift+E）插入表情符號，或輸入 `:` 觸發行內自動完成
- **Paste image from clipboard / 從剪貼簿貼上圖片** — Ctrl+V pastes clipboard images, saves to file, and inserts Markdown image reference / Ctrl+V 貼上剪貼簿圖片，儲存至檔案並插入 Markdown 圖片參照
- **Local image preview / 本地圖片預覽** — Relative image paths resolve correctly in the preview via virtual host mapping / 相對圖片路徑透過虛擬主機對應在預覽中正確顯示
- **List editing / 列表編輯** — Auto-continue bullet, numbered, and task lists on Enter; toggle bullet list (Ctrl+Shift+U) or numbered list (Ctrl+Shift+N); indent/outdent with Tab/Shift+Tab / 按 Enter 自動延續項目符號、編號及任務列表；使用 Ctrl+Shift+U 切換項目符號列表或 Ctrl+Shift+N 切換編號列表；使用 Tab/Shift+Tab 縮排／取消縮排
- **Font picker / 字型選擇器** — Toolbar dropdowns to change editor font (monospace) and preview font (sans-serif), persisted in settings / 工具列下拉選單可變更編輯器字型（等寬）與預覽字型（無襯線），設定會持久保存
- **Settings persistence / 設定持久化** — Window layout, theme, font size, font family, language, and scroll sync preference are remembered across sessions / 視窗佈局、佈景主題、字型大小、字型、語言及同步捲動偏好跨工作階段記憶

## Keyboard Shortcuts / 鍵盤快速鍵

| Shortcut / 快速鍵 | Action / 動作 |
|---|---|
| Ctrl+N | New file / 新增檔案 |
| Ctrl+O | Open file / 開啟檔案 |
| Ctrl+S | Save / 儲存 |
| Ctrl+Shift+S | Save As / 另存新檔 |
| Ctrl+Z / Ctrl+Y | Undo / Redo / 復原／重做 |
| Ctrl+F | Find / 尋找 |
| Ctrl+H | Replace / 取代 |
| Ctrl+T | Toggle light/dark theme / 切換亮色／暗色佈景主題 |
| Ctrl+L | Toggle sync scrolling / 切換同步捲動 |
| Ctrl+Shift+C | Insert Alert block / 插入提示區塊 |
| Ctrl+Shift+T | Insert Table / 插入表格 |
| Ctrl+Shift+O | Insert TOC / 插入目錄 |
| Ctrl+Shift+D | Toggle TOC in preview / 切換預覽目錄 |
| Ctrl+Shift+E | Insert Emoji / 插入表情符號 |
| Ctrl+Shift+U | Toggle bullet list / 切換項目符號列表 |
| Ctrl+Shift+N | Toggle numbered list / 切換編號列表 |
| Tab | Indent list item / 縮排列表項目 |
| Shift+Tab | Outdent list item / 取消縮排列表項目 |
| Enter | Auto-continue list / 自動延續列表 |
| Ctrl+M | Toggle preview-only mode / 切換僅預覽模式 |
| Ctrl+= / Ctrl+- | Zoom in / out / 放大／縮小 |
| Ctrl+0 | Reset zoom / 重設縮放 |
| Ctrl+Scroll | Zoom with mouse wheel / 滑鼠滾輪縮放 |
| Ctrl+E | Export HTML / 匯出 HTML |
| Ctrl+P | Export PDF / 匯出 PDF |
| F1 | Keyboard shortcuts / 鍵盤快速鍵 |
| Ctrl+Q | Exit / 結束 |

## Toolbar / 工具列

| Icon | Function / 功能 | Shortcut / 快速鍵 |
|:---:|---|---|
| **B** | Bold / 粗體 | Ctrl+B |
| *I* | Italic / 斜體 | Ctrl+I |
| ~~S~~ | Strikethrough / 刪除線 | Ctrl+Shift+5 |
| ❝ | Blockquote / 引用 | Ctrl+Shift+. |
| `</>` | Inline Code / 行內程式碼 | Ctrl+Shift+K |
| `{}` | Code Fence / 程式碼區塊 | — |
| • — | Bullet List / 項目符號列表 | Ctrl+Shift+U |
| 1. — | Numbered List / 編號列表 | Ctrl+Shift+N |
| ❎ | Task List / 任務列表 | Ctrl+Shift+X |
| ⚠ | Insert Alert / 插入提示區塊 | Ctrl+Shift+C |
| 🖼 | Insert Image / 插入圖片 | — |
| ⊞ | Insert Table / 插入表格 | Ctrl+Shift+T |
| ☰ | Insert TOC / 插入目錄 | Ctrl+Shift+O |
| 😀 | Emoji Picker / 表情符號選擇器 | Ctrl+Shift+E |
| ⇄ | CSV ⇄ Table Toggle / CSV⇄表格轉換 | Ctrl+Shift+V |
| 🔄 | Force Refresh / 強制重新整理 | — |
| ☑ Preview Only | Toggle preview-only mode / 切換僅預覽模式 | Ctrl+M |
| ☑ TOC | Toggle TOC in preview / 切換預覽目錄 | Ctrl+Shift+D |
| ☑ Sync | Toggle sync scrolling / 切換同步捲動 | Ctrl+L |
| ☑ Dark Mode | Toggle light/dark theme / 切換亮色／暗色佈景主題 | Ctrl+T |
| A Consolas ▾ | Editor Font / 編輯器字型 | — |
| A Default ▾ | Preview Font / 預覽字型 | — |
| 🌐 EN/中文 | Switch Language / 切換語言 | — |

## Requirements / 系統需求

- Windows 10/11 (64-bit) / Windows 10/11（64 位元）
- [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/) (included with modern Windows) / [WebView2 執行階段](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)（現代 Windows 已內建）

## Build / 建置

```bash
# Debug build / 除錯建置
dotnet build

# Release build / 發行建置
dotnet build -c Release

# Publish self-contained single-file executable / 發佈獨立單檔執行檔
dotnet publish -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -o bin/Release/net8.0-windows/publish/win-x64
```

An [Inno Setup](https://jrsoftware.org/isinfo.php) script (`publish.iss`) is included to create an installer with file associations and Start Menu/Desktop shortcuts.

附有 [Inno Setup](https://jrsoftware.org/isinfo.php) 腳本（`publish.iss`），可建立包含檔案關聯及開始功能表／桌面捷徑的安裝程式。

## Tech Stack / 技術堆疊

- **.NET 8.0** — WPF desktop application (MVVM) / WPF 桌面應用程式（MVVM）
- **CommunityToolkit.Mvvm** — MVVM source generators (`ObservableObject`, `RelayCommand`) / MVVM 原始碼產生器
- **Microsoft.Xaml.Behaviors.Wpf** — XAML behaviors for decoupled event handling / XAML 行為，用於解耦事件處理
- **AvalonEdit** — Code editor component / 程式碼編輯器元件
- **WebView2** — Chromium-based preview rendering / 基於 Chromium 的預覽渲染
- **Markdig** — Markdown to HTML conversion (advanced extensions enabled) / Markdown 轉 HTML（啟用進階擴充）

---

## Copyright / 版權聲明

<img src="Assets/winstrong_logo.png" alt="Winstrong Technology / 耘強科技" width="200">

Copyright &copy; 2025 Winstrong Technology, Taiwan. All rights reserved.

版權所有 &copy; 2025 耘強科技，台灣。保留一切權利。

Author / 作者: Bill Wang (billwang168@gmail.com)
