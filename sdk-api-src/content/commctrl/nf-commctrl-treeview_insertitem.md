---
UID: NF:commctrl.TreeView_InsertItem
title: TreeView_InsertItem macro (commctrl.h)
description: Inserts a new item in a tree-view control. You can use this macro or send the TVM_INSERTITEM message explicitly.
helpviewer_keywords: ["TreeView_InsertItem","TreeView_InsertItem macro [Windows Controls]","_win32_TreeView_InsertItem","_win32_TreeView_InsertItem_cpp","commctrl/TreeView_InsertItem","controls.TreeView_InsertItem","controls._win32_TreeView_InsertItem"]
old-location: controls\TreeView_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_insertitem.htm
ms.date: 10/21/2024
ms.keywords: TreeView_InsertItem, TreeView_InsertItem macro [Windows Controls], _win32_TreeView_InsertItem, _win32_TreeView_InsertItem_cpp, commctrl/TreeView_InsertItem, controls.TreeView_InsertItem, controls._win32_TreeView_InsertItem
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
 - TreeView_InsertItem
 - commctrl/TreeView_InsertItem
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
 - TreeView_InsertItem
---

# TreeView_InsertItem macro

## -syntax

```cpp
HTREEITEM TreeView_InsertItem(
   HWND             hwnd,
   LPTVINSERTSTRUCT lpis
);
```

## -returns

Type: **HTREEITEM**

Returns the <b>HTREEITEM</b> handle to the new item if successful, or <b>NULL</b> otherwise.


## -description

Inserts a new item in a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-insertitem">TVM_INSERTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param lpis

Type: <b>LPTVINSERTSTRUCT</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-tvinsertstructa">TVINSERTSTRUCT</a> structure that specifies the attributes of the tree-view item.

## -see-also

<a href="/windows/desktop/Controls/tvn-endlabeledit">TVN_ENDLABELEDIT</a>
