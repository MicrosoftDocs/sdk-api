---
UID: NF:commctrl.TreeView_Expand
title: TreeView_Expand macro (commctrl.h)
description: The TreeView_Expand macro expands or collapses the list of child items associated with the specified parent item, if any. You can use this macro or send the TVM_EXPAND message explicitly.
helpviewer_keywords: ["TreeView_Expand","TreeView_Expand macro [Windows Controls]","_win32_TreeView_Expand","_win32_TreeView_Expand_cpp","commctrl/TreeView_Expand","controls.TreeView_Expand","controls._win32_TreeView_Expand"]
old-location: controls\TreeView_Expand.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_expand.htm
ms.date: 10/21/2024
ms.keywords: TreeView_Expand, TreeView_Expand macro [Windows Controls], _win32_TreeView_Expand, _win32_TreeView_Expand_cpp, commctrl/TreeView_Expand, controls.TreeView_Expand, controls._win32_TreeView_Expand
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
 - TreeView_Expand
 - commctrl/TreeView_Expand
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
 - TreeView_Expand
---

# TreeView_Expand macro

## -syntax

```cpp
BOOL TreeView_Expand(
   HWND      hwnd,
   HTREEITEM hitem,
   UINT      code
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if the operation was successful, or zero otherwise.


## -description

The <b>TreeView_Expand</b> macro expands or collapses the list of child items associated with the specified parent item, if any. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-expand">TVM_EXPAND</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to the parent item that will be expanded or collapsed.

### -param code

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Action flag. For a list of possible values, see the description of the <i>wParam</i> parameter in <a href="/windows/desktop/Controls/tvm-expand">TVM_EXPAND</a>.

## -remarks

Expanding a node that is already expanded, or collapsing a node that is already collapsed is considered a successful operation and the macro returns a nonzero value. Attempting to expand or collapse a node that has no children is considered a failure and the return value is zero. 

When an item is first expanded by a <a href="/windows/desktop/Controls/tvm-expand">TVM_EXPAND</a> message, the action generates <a href="/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a> and <a href="/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a> notification codes and the item's <a href="/windows/desktop/Controls/tree-view-control-item-states">TVIS_EXPANDEDONCE</a> state flag is set. As long as this state flag remains set, subsequent <b>TVM_EXPAND</b> messages do not generate TVN_ITEMEXPANDING or TVN_ITEMEXPANDED notifications. To reset the <b>TVIS_EXPANDEDONCE</b> state flag, you must send a <b>TVM_EXPAND</b> message with the TVE_COLLAPSE and TVE_COLLAPSERESET flags set. Attempting to explicitly set <b>TVIS_EXPANDEDONCE</b> will result in unpredictable behavior.

The expand operation may fail if the owner of the treeview control denies the operation in response to a <a href="/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a> notification.
