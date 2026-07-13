---
UID: NF:commctrl.TreeView_SetInsertMark
title: TreeView_SetInsertMark macro (commctrl.h)
description: Sets the insertion mark in a tree-view control. You can use this macro or send the TVM_SETINSERTMARK message explicitly.
helpviewer_keywords: ["TreeView_SetInsertMark","TreeView_SetInsertMark macro [Windows Controls]","_win32_TreeView_SetInsertMark","_win32_TreeView_SetInsertMark_cpp","commctrl/TreeView_SetInsertMark","controls.TreeView_SetInsertMark","controls._win32_TreeView_SetInsertMark"]
old-location: controls\TreeView_SetInsertMark.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setinsertmark.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetInsertMark, TreeView_SetInsertMark macro [Windows Controls], _win32_TreeView_SetInsertMark, _win32_TreeView_SetInsertMark_cpp, commctrl/TreeView_SetInsertMark, controls.TreeView_SetInsertMark, controls._win32_TreeView_SetInsertMark
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
 - TreeView_SetInsertMark
 - commctrl/TreeView_SetInsertMark
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
 - TreeView_SetInsertMark
---

# TreeView_SetInsertMark macro

## -syntax

```cpp
BOOL TreeView_SetInsertMark(
   HWND      hwnd,
   HTREEITEM hItem,
   BOOL      fAfter
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Sets the insertion mark in a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setinsertmark">TVM_SETINSERTMARK</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param hItem

Type: <b>HTREEITEM</b>

<b>HTREEITEM</b> that specifies at which item the insertion mark will be placed. If this argument is <b>NULL</b>, the insertion mark is removed.

### -param fAfter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>BOOL</b> value that specifies if the insertion mark is placed before or after the specified item. If this argument is nonzero, the insertion mark will be placed after the item. If this argument is zero, the insertion mark will be placed before the item.
