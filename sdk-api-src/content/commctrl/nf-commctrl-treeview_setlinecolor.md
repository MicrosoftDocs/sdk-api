---
UID: NF:commctrl.TreeView_SetLineColor
title: TreeView_SetLineColor macro (commctrl.h)
description: Sets the current line color. You can also use the TVM_SETLINECOLOR message directly.
helpviewer_keywords: ["TreeView_SetLineColor","TreeView_SetLineColor macro [Windows Controls]","_win32_TreeView_SetLineColor","_win32_TreeView_SetLineColor_cpp","commctrl/TreeView_SetLineColor","controls.TreeView_SetLineColor","controls._win32_TreeView_SetLineColor"]
old-location: controls\TreeView_SetLineColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setlinecolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetLineColor, TreeView_SetLineColor macro [Windows Controls], _win32_TreeView_SetLineColor, _win32_TreeView_SetLineColor_cpp, commctrl/TreeView_SetLineColor, controls.TreeView_SetLineColor, controls._win32_TreeView_SetLineColor
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
 - TreeView_SetLineColor
 - commctrl/TreeView_SetLineColor
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
 - TreeView_SetLineColor
---

# TreeView_SetLineColor macro

## -syntax

```cpp
COLORREF TreeView_SetLineColor(
   HWND     hwnd,
   COLORREF clr
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns the previous line color.


## -description

Sets the current line color. You can also use the <a href="/windows/desktop/Controls/tvm-setlinecolor">TVM_SETLINECOLOR</a> message directly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param clr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

A <a href="/windows/desktop/gdi/colorref">COLORREF</a> that specifies the new line color. Use the CLR_DEFAULT value to restore the system default colors.

## -remarks

This message only changes line colors. To change the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_settextcolor">TreeView_SetTextColor</a> macro.

## -see-also

<a href="/windows/desktop/Controls/tvm-setlinecolor">TVM_SETLINECOLOR</a>
