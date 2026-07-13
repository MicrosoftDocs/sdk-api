---
UID: NF:commctrl.TreeView_SortChildrenCB
title: TreeView_SortChildrenCB macro (commctrl.h)
description: Sorts tree-view items using an application-defined callback function that compares the items. You can use this macro or send the TVM_SORTCHILDRENCB message explicitly.
helpviewer_keywords: ["TreeView_SortChildrenCB","TreeView_SortChildrenCB macro [Windows Controls]","_win32_TreeView_SortChildrenCB","_win32_TreeView_SortChildrenCB_cpp","commctrl/TreeView_SortChildrenCB","controls.TreeView_SortChildrenCB","controls._win32_TreeView_SortChildrenCB"]
old-location: controls\TreeView_SortChildrenCB.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_sortchildrencb.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SortChildrenCB, TreeView_SortChildrenCB macro [Windows Controls], _win32_TreeView_SortChildrenCB, _win32_TreeView_SortChildrenCB_cpp, commctrl/TreeView_SortChildrenCB, controls.TreeView_SortChildrenCB, controls._win32_TreeView_SortChildrenCB
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
 - TreeView_SortChildrenCB
 - commctrl/TreeView_SortChildrenCB
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
 - TreeView_SortChildrenCB
---

# TreeView_SortChildrenCB macro

## -syntax

```cpp
BOOL TreeView_SortChildrenCB(
   HWND       hwnd,
   LPTVSORTCB psort,
   BOOL       recurse
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sorts tree-view items using an application-defined callback function that compares the items. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-sortchildrencb">TVM_SORTCHILDRENCB</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param psort

Type: <b>LPTVSORTCB</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-tvsortcb">TVSORTCB</a> structure. The <b>lpfnCompare</b> member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared. For more information about the callback function, see the description of <b>TVSORTCB</b>.

### -param recurse

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Reserved. Must be zero.
