---
UID: NF:commctrl.TreeView_GetInsertMarkColor
title: TreeView_GetInsertMarkColor macro (commctrl.h)
description: Retrieves the color used to draw the insertion mark for the tree view. You can use this macro or send the TVM_GETINSERTMARKCOLOR message explicitly.
helpviewer_keywords: ["TreeView_GetInsertMarkColor","TreeView_GetInsertMarkColor macro [Windows Controls]","_win32_TreeView_GetInsertMarkColor","_win32_TreeView_GetInsertMarkColor_cpp","commctrl/TreeView_GetInsertMarkColor","controls.TreeView_GetInsertMarkColor","controls._win32_TreeView_GetInsertMarkColor"]
old-location: controls\TreeView_GetInsertMarkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getinsertmarkcolor.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetInsertMarkColor, TreeView_GetInsertMarkColor macro [Windows Controls], _win32_TreeView_GetInsertMarkColor, _win32_TreeView_GetInsertMarkColor_cpp, commctrl/TreeView_GetInsertMarkColor, controls.TreeView_GetInsertMarkColor, controls._win32_TreeView_GetInsertMarkColor
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
 - TreeView_GetInsertMarkColor
 - commctrl/TreeView_GetInsertMarkColor
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
 - TreeView_GetInsertMarkColor
---

# TreeView_GetInsertMarkColor macro

## -syntax

```cpp
COLORREF TreeView_GetInsertMarkColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that contains the current insertion mark color.

## -description

Retrieves the color used to draw the insertion mark for the tree view. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getinsertmarkcolor">TVM_GETINSERTMARKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_setinsertmarkcolor">TreeView_SetInsertMarkColor</a>
