---
UID: NF:commctrl.TreeView_GetBkColor
title: TreeView_GetBkColor macro (commctrl.h)
description: Retrieves the current background color of the control. You can use this macro or send the TVM_GETBKCOLOR message explicitly.
helpviewer_keywords: ["TreeView_GetBkColor","TreeView_GetBkColor macro [Windows Controls]","_win32_TreeView_GetBkColor","_win32_TreeView_GetBkColor_cpp","commctrl/TreeView_GetBkColor","controls.TreeView_GetBkColor","controls._win32_TreeView_GetBkColor"]
old-location: controls\TreeView_GetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getbkcolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetBkColor, TreeView_GetBkColor macro [Windows Controls], _win32_TreeView_GetBkColor, _win32_TreeView_GetBkColor_cpp, commctrl/TreeView_GetBkColor, controls.TreeView_GetBkColor, controls._win32_TreeView_GetBkColor
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
 - TreeView_GetBkColor
 - commctrl/TreeView_GetBkColor
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
 - TreeView_GetBkColor
---

# TreeView_GetBkColor macro

## -syntax

```cpp
COLORREF TreeView_GetBkColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

<p>Returns a <b>COLORREF</b> value that represents the current background color. If this value is -1, the control is using the system color for the background color.

## -description

Retrieves the current background color of the control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getbkcolor">TVM_GETBKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_setbkcolor">TreeView_SetBkColor</a>
