---
UID: NF:commctrl.TreeView_SetTextColor
title: TreeView_SetTextColor macro (commctrl.h)
description: Sets the text color of the control. You can use this macro or send the TVM_SETTEXTCOLOR message explicitly.
helpviewer_keywords: ["TreeView_SetTextColor","TreeView_SetTextColor macro [Windows Controls]","_win32_TreeView_SetTextColor","_win32_TreeView_SetTextColor_cpp","commctrl/TreeView_SetTextColor","controls.TreeView_SetTextColor","controls._win32_TreeView_SetTextColor"]
old-location: controls\TreeView_SetTextColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_settextcolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetTextColor, TreeView_SetTextColor macro [Windows Controls], _win32_TreeView_SetTextColor, _win32_TreeView_SetTextColor_cpp, commctrl/TreeView_SetTextColor, controls.TreeView_SetTextColor, controls._win32_TreeView_SetTextColor
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
 - TreeView_SetTextColor
 - commctrl/TreeView_SetTextColor
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
 - TreeView_SetTextColor
---

# TreeView_SetTextColor macro

## -syntax

```cpp
COLORREF TreeView_SetTextColor(
   HWND     hwnd,
   COLORREF clr
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that represents the previous text color. If this value is -1, the control was using the system color for the text color.


## -description

Sets the text color of the control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-settextcolor">TVM_SETTEXTCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param clr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="/windows/desktop/gdi/colorref">COLORREF</a> value that contains the new text color. If this argument is -1, the control will revert to using the system color for the text color.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_gettextcolor">TreeView_GetTextColor</a>
