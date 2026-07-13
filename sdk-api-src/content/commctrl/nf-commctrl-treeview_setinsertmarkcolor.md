---
UID: NF:commctrl.TreeView_SetInsertMarkColor
title: TreeView_SetInsertMarkColor macro (commctrl.h)
description: Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the TVM_SETINSERTMARKCOLOR message explicitly.
helpviewer_keywords: ["TreeView_SetInsertMarkColor","TreeView_SetInsertMarkColor macro [Windows Controls]","_win32_TreeView_SetInsertMarkColor","_win32_TreeView_SetInsertMarkColor_cpp","commctrl/TreeView_SetInsertMarkColor","controls.TreeView_SetInsertMarkColor","controls._win32_TreeView_SetInsertMarkColor"]
old-location: controls\TreeView_SetInsertMarkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setinsertmarkcolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetInsertMarkColor, TreeView_SetInsertMarkColor macro [Windows Controls], _win32_TreeView_SetInsertMarkColor, _win32_TreeView_SetInsertMarkColor_cpp, commctrl/TreeView_SetInsertMarkColor, controls.TreeView_SetInsertMarkColor, controls._win32_TreeView_SetInsertMarkColor
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
 - TreeView_SetInsertMarkColor
 - commctrl/TreeView_SetInsertMarkColor
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
 - TreeView_SetInsertMarkColor
---

# TreeView_SetInsertMarkColor macro

## -syntax

```cpp
COLORREF TreeView_SetInsertMarkColor(
   HWND     hwnd,
   COLORREF clr
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that contains the previous insertion mark color.


## -description

Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setinsertmarkcolor">TVM_SETINSERTMARKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param clr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="/windows/desktop/gdi/colorref">COLORREF</a> value that contains the new insertion mark color.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getinsertmarkcolor">TreeView_GetInsertMarkColor</a>
