---
UID: NF:commctrl.TreeView_SetItemState
title: TreeView_SetItemState macro (commctrl.h)
description: Sets a tree-view item's state attributes. You can use this macro or send the TVM_SETITEM message explicitly.
helpviewer_keywords: ["TreeView_SetItemState","TreeView_SetItemState macro [Windows Controls]","_win32_TreeView_SetItemState","_win32_TreeView_SetItemState_cpp","commctrl/TreeView_SetItemState","controls.TreeView_SetItemState","controls._win32_TreeView_SetItemState"]
old-location: controls\TreeView_SetItemState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setitemstate.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetItemState, TreeView_SetItemState macro [Windows Controls], _win32_TreeView_SetItemState, _win32_TreeView_SetItemState_cpp, commctrl/TreeView_SetItemState, controls.TreeView_SetItemState, controls._win32_TreeView_SetItemState
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
 - TreeView_SetItemState
 - commctrl/TreeView_SetItemState
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
 - TreeView_SetItemState
---

# TreeView_SetItemState macro

## -syntax

```cpp
UINT TreeView_SetItemState(
   HWND      hwndTV,
   HTREEITEM hti,
   UINT      data,
   UINT      _mask
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The return value is not used.


## -description

Sets a tree-view item's state attributes. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setitem">TVM_SETITEM</a> message explicitly.

## -parameters

### -param hwndTV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hti

Type: <b>HTREEITEM</b>

Handle to the item.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value that is equivalent to the <b>data</b> member of <a href="/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a>.

### -param _mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Mask used to select the states to be set. It is equivalent to the <b>_mask</b> member of <a href="/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a>.
