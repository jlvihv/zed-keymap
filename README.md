```json
[
  {
    "context": "Editor && (vim_mode == normal || vim_mode == visual) && !VimWaiting && !menu",
    "bindings": {
      // put key-bindings here if you want them to work in normal & visual mode
      // 跳到行尾
      "g l": "vim::EndOfLine",
      // 跳到行首
      "g h": "vim::FirstNonWhitespace",
      // ge 文档底部
      "g e": "vim::EndOfDocument"
    }
  },
  {
    "context": "Editor && vim_mode == normal && !VimWaiting && !menu",
    "bindings": {
      // put key-bindings here if you want them to work only in normal mode
      // gb 回到上一个位置
      "g b": "pane::GoBack",
      // gr 转到引用
      "g r": "editor::FindAllReferences",
      // gi 转到实现
      "g i": "editor::GoToImplementation",
      // 格式化
      "space f m": "editor::Format",
      // 全局搜索
      "space f w": "pane::DeploySearch",
      // 文件名搜索
      "space f f": "file_finder::Toggle",
      // 重命名
      "space r": "editor::Rename",
      // 保存
      "space w": "workspace::Save",
      // 关闭当前页
      "space c": "pane::CloseActiveItem",
      // 关闭所有页
      "space g c": "pane::CloseAllItems",
      // 退出
      "space q": "workspace::CloseWindow",
      // 上一个标签页
      "H": "pane::ActivatePrevItem",
      // 下一个标签页
      "L": "pane::ActivateNextItem",
      // 聚焦到文件树
      "space e": "project_panel::ToggleFocus",
      // 关闭左侧文件栏
      "space b": "workspace::ToggleLeftDock",
      // 切换右侧 AI Chat 栏
      "space i": "workspace::ToggleRightDock",
      // 快速修复 | 代码动作
      "space .": "editor::ToggleCodeActions"
    }
  },
  {
    "context": "Editor && vim_mode == visual && !VimWaiting && !menu",
    "bindings": {
      // visual, visual line & visual block modes
    }
  },
  {
    "context": "Editor && vim_mode == insert && !menu",
    "bindings": {
      // put key-bindings here if you want them to work in insert mode
      // e.g.
      // "j j": "vim::NormalBefore" // remap jj in insert mode to escape.
      "j k": ["vim::SwitchMode", "Normal"]
    }
  },
  {
    // netrw compatibility
    "context": "ProjectPanel && not_editing",
    "bindings": {
      // 新建文件
      "a": "project_panel::NewFile",
      // 新建文件夹
      "A": "project_panel::NewDirectory",
      // 重命名
      "r": "project_panel::Rename",
      // 放到回收站
      "d": "project_panel::Trash",
      // 删除
      "D": "project_panel::Delete",
      // 复制
      "y": "project_panel::Copy",
      // 剪切
      "x": "project_panel::Cut",
      // 粘贴
      "p": "project_panel::Paste",
      // 在文件管理器中显示
      "O": "project_panel::RevealInFinder"
    }
  },
  {
    "context": "Editor && (showing_code_actions || showing_completions)",
    "bindings": {
      // 使用 tab 键切换代码建议
      "shift-tab": "editor::ContextMenuPrev",
      "tab": "editor::ContextMenuNext"
    }
  },
  {
    "context": "Terminal",
    "bindings": {
      // 打开 / 关闭终端
      "ctrl-`": "workspace::ToggleBottomDock"
    }
  },
  {
    "context": "ConversationEditor > Editor",
    "bindings": {
      // 给 AI 助手发送消息
      "alt-enter": "assistant::Assist"
    }
  }
]
```
