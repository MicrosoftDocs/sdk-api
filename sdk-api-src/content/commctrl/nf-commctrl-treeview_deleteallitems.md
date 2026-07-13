---
UID: NF:commctrl.TreeView_DeleteAllItems
title: TreeView_DeleteAllItems macro (commctrl.h)
description: Deletes all items from a tree-view control.
helpviewer_keywords: ["TreeView_DeleteAllItems","TreeView_DeleteAllItems macro [Windows Controls]","_win32_TreeView_DeleteAllItems","_win32_TreeView_DeleteAllItems_cpp","commctrl/TreeView_DeleteAllItems","controls.TreeView_DeleteAllItems","controls._win32_TreeView_DeleteAllItems"]
old-location: controls\TreeView_DeleteAllItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_deleteallitems.htm
ms.date: 10/21/2024
ms.keywords: TreeView_DeleteAllItems, TreeView_DeleteAllItems macro [Windows Controls], _win32_TreeView_DeleteAllItems, _win32_TreeView_DeleteAllItems_cpp, commctrl/TreeView_DeleteAllItems, controls.TreeView_DeleteAllItems, controls._win32_TreeView_DeleteAllItems
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
 - TreeView_DeleteAllItems
 - commctrl/TreeView_DeleteAllItems
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
 - TreeView_DeleteAllItems
---

# TreeView_DeleteAllItems macro

## -syntax

```cpp
BOOL TreeView_DeleteAllItems(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Deletes all items from a tree-view control.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -remarks

Once an item is deleted from a tree-view control, its <b>HTREEITEM</b> handle is invalid and cannot be used.

The parent window receives a <a href="/windows/desktop/Controls/tvn-deleteitem">TVN_DELETEITEM</a> notification code when each item is removed.

If the item label is being edited, the edit operation is canceled and the parent window receives the <a href="/windows/desktop/Controls/tvn-endlabeledit">TVN_ENDLABELEDIT</a> notification code. 

You can also delete all items with the <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_deleteitem">TreeView_DeleteItem</a> macro or the <a href="/windows/desktop/Controls/tvm-deleteitem">TVM_DELETEITEM</a> message by setting 
				<i>lParam</i> to TVI_ROOT.

If the window style for a tree-view control contains TVS_NOSCROLL and all items are deleted, new items are not displayed until the window styles are reset. The following code shows one way to ensure that items are always displayed.



```
DWORD styles = GetWindowLong(hwnd, GWL_STYLE);
TreeView_DeleteAllItems(hwnd);
SetWindowLong(hwnd, GWL_STYLE, styles);
```
