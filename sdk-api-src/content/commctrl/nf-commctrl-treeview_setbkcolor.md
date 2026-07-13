---
UID: NF:commctrl.TreeView_SetBkColor
title: TreeView_SetBkColor macro (commctrl.h)
description: Sets the background color of the control. You can use this macro or send the TVM_SETBKCOLOR message explicitly.
helpviewer_keywords: ["TreeView_SetBkColor","TreeView_SetBkColor macro [Windows Controls]","_win32_TreeView_SetBkColor","_win32_TreeView_SetBkColor_cpp","commctrl/TreeView_SetBkColor","controls.TreeView_SetBkColor","controls._win32_TreeView_SetBkColor"]
old-location: controls\TreeView_SetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setbkcolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetBkColor, TreeView_SetBkColor macro [Windows Controls], _win32_TreeView_SetBkColor, _win32_TreeView_SetBkColor_cpp, commctrl/TreeView_SetBkColor, controls.TreeView_SetBkColor, controls._win32_TreeView_SetBkColor
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
 - TreeView_SetBkColor
 - commctrl/TreeView_SetBkColor
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
 - TreeView_SetBkColor
---

# TreeView_SetBkColor macro

## -syntax

```cpp
COLORREF TreeView_SetBkColor(
   HWND     hwnd,
   COLORREF clr
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that represents the previous background color. If this value is -1, the control was using the system color for the background color.


## -description

Sets the background color of the control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setbkcolor">TVM_SETBKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param clr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="/windows/desktop/gdi/colorref">COLORREF</a> value that contains the new background color. If this argument is -1, the control will revert to using the system color for the background color.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getbkcolor">TreeView_GetBkColor</a>
