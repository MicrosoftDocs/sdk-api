---
UID: NF:commctrl.TreeView_GetExtendedStyle
title: TreeView_GetExtendedStyle macro (commctrl.h)
description: Retrieves the extended style for a specified tree-view control. Use this macro or send the TVM_GETEXTENDEDSTYLE message explicitly.
helpviewer_keywords: ["TreeView_GetExtendedStyle","TreeView_GetExtendedStyle macro [Windows Controls]","_shell_TreeView_GetExtendedStyle","_shell_TreeView_GetExtendedStyle_cpp","commctrl/TreeView_GetExtendedStyle","controls.TreeView_GetExtendedStyle","controls._shell_TreeView_GetExtendedStyle"]
old-location: controls\TreeView_GetExtendedStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getextendedstyle.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetExtendedStyle, TreeView_GetExtendedStyle macro [Windows Controls], _shell_TreeView_GetExtendedStyle, _shell_TreeView_GetExtendedStyle_cpp, commctrl/TreeView_GetExtendedStyle, controls.TreeView_GetExtendedStyle, controls._shell_TreeView_GetExtendedStyle
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TreeView_GetExtendedStyle
 - commctrl/TreeView_GetExtendedStyle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_GetExtendedStyle
---

# TreeView_GetExtendedStyle macro

## -syntax

```cpp
DWORD TreeView_GetExtendedStyle(
   HWND hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the value of extended style. For more information on styles, see <a href="/windows/win32/controls/tree-view-control-window-extended-styles">Tree-View Control Extended Styles</a>.

## -description

Retrieves the extended style for a specified tree-view control. Use this macro or send the <a href="/windows/desktop/Controls/tvm-getextendedstyle">TVM_GETEXTENDEDSTYLE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -remarks

The extended styles for a tree-view control have nothing to do with the extended styles used with function <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> or function <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>.
