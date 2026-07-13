---
UID: NF:commctrl.TreeView_GetItemState
title: TreeView_GetItemState macro (commctrl.h)
description: Retrieves some or all of a tree-view item's state attributes. You can use this macro or send the TVM_GETITEMSTATE message explicitly.
helpviewer_keywords: ["TreeView_GetItemState","TreeView_GetItemState macro [Windows Controls]","_win32_TreeView_GetItemState","_win32_TreeView_GetItemState_cpp","commctrl/TreeView_GetItemState","controls.TreeView_GetItemState","controls._win32_TreeView_GetItemState"]
old-location: controls\TreeView_GetItemState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitemstate.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetItemState, TreeView_GetItemState macro [Windows Controls], _win32_TreeView_GetItemState, _win32_TreeView_GetItemState_cpp, commctrl/TreeView_GetItemState, controls.TreeView_GetItemState, controls._win32_TreeView_GetItemState
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
 - TreeView_GetItemState
 - commctrl/TreeView_GetItemState
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
 - TreeView_GetItemState
---

# TreeView_GetItemState macro

## -syntax

```cpp
UINT TreeView_GetItemState(
   HWND      hwndTV,
   HTREEITEM hti,
   UINT      mask
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns a <b>UINT</b> value that is equivalent to the state member of <b>TVITEMEX</b>. The state bits that are both true and were specified in <b>mask</b> will be set.


## -description

Retrieves some or all of a tree-view item's state attributes. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getitemstate">TVM_GETITEMSTATE</a> message explicitly.

## -parameters

### -param hwndTV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hti

Type: <b>HTREEITEM</b>

Handle to the item.

### -param mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Mask used to specify the states to query for. It is equivalent to the <b>mask</b> member of <a href="/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a>.
