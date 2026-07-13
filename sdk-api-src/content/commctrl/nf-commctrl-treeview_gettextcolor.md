---
UID: NF:commctrl.TreeView_GetTextColor
title: TreeView_GetTextColor macro (commctrl.h)
description: Retrieves the current text color of the control. You can use this macro or send the TVM_GETTEXTCOLOR message explicitly.
helpviewer_keywords: ["TreeView_GetTextColor","TreeView_GetTextColor macro [Windows Controls]","_win32_TreeView_GetTextColor","_win32_TreeView_GetTextColor_cpp","commctrl/TreeView_GetTextColor","controls.TreeView_GetTextColor","controls._win32_TreeView_GetTextColor"]
old-location: controls\TreeView_GetTextColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_gettextcolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetTextColor, TreeView_GetTextColor macro [Windows Controls], _win32_TreeView_GetTextColor, _win32_TreeView_GetTextColor_cpp, commctrl/TreeView_GetTextColor, controls.TreeView_GetTextColor, controls._win32_TreeView_GetTextColor
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - TreeView_GetTextColor
 - commctrl/TreeView_GetTextColor
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
 - TreeView_GetTextColor
---

# TreeView_GetTextColor macro

## -syntax

```cpp
COLORREF TreeView_GetTextColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that represents the current text color. If this value is -1, the control is using the system color for the text color.


## -description

Retrieves the current text color of the control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-gettextcolor">TVM_GETTEXTCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_settextcolor">TreeView_SetTextColor</a>
