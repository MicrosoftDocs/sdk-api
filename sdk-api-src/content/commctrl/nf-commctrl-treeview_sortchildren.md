---
UID: NF:commctrl.TreeView_SortChildren
title: TreeView_SortChildren macro (commctrl.h)
description: Sorts the child items of the specified parent item in a tree-view control. You can use this macro or send the TVM_SORTCHILDREN message explicitly.
helpviewer_keywords: ["TreeView_SortChildren","TreeView_SortChildren macro [Windows Controls]","_win32_TreeView_SortChildren","_win32_TreeView_SortChildren_cpp","commctrl/TreeView_SortChildren","controls.TreeView_SortChildren","controls._win32_TreeView_SortChildren"]
old-location: controls\TreeView_SortChildren.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_sortchildren.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SortChildren, TreeView_SortChildren macro [Windows Controls], _win32_TreeView_SortChildren, _win32_TreeView_SortChildren_cpp, commctrl/TreeView_SortChildren, controls.TreeView_SortChildren, controls._win32_TreeView_SortChildren
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
 - TreeView_SortChildren
 - commctrl/TreeView_SortChildren
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
 - TreeView_SortChildren
---

# TreeView_SortChildren macro

## -syntax

```cpp
BOOL TreeView_SortChildren(
   HWND      hwnd,
   HTREEITEM hitem,
   BOOL      recurse
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sorts the child items of the specified parent item in a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-sortchildren">TVM_SORTCHILDREN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to the parent item whose child items are to be sorted.

### -param recurse

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Not implemented; see remarks.

## -remarks

This message alphabetizes the tree items using <a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a> on the item name. You can use the <a href="/windows/desktop/Controls/tvm-sortchildrencb">TVM_SORTCHILDRENCB</a> message to customize the ordering behavior.
