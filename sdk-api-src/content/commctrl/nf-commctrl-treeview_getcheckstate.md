---
UID: NF:commctrl.TreeView_GetCheckState
title: TreeView_GetCheckState macro (commctrl.h)
description: Gets the check state of the specified item. You can also use the TVM_GETITEMSTATE message directly.
helpviewer_keywords: ["TreeView_GetCheckState","TreeView_GetCheckState macro [Windows Controls]","_win32_TreeView_GetCheckState","_win32_TreeView_GetCheckState_cpp","commctrl/TreeView_GetCheckState","controls.TreeView_GetCheckState","controls._win32_TreeView_GetCheckState"]
old-location: controls\TreeView_GetCheckState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getcheckstate.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetCheckState, TreeView_GetCheckState macro [Windows Controls], _win32_TreeView_GetCheckState, _win32_TreeView_GetCheckState_cpp, commctrl/TreeView_GetCheckState, controls.TreeView_GetCheckState, controls._win32_TreeView_GetCheckState
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
 - TreeView_GetCheckState
 - commctrl/TreeView_GetCheckState
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
 - TreeView_GetCheckState
---

# TreeView_GetCheckState macro

## -syntax

```cpp
UINT TreeView_GetCheckState(
   HWND      hwndTV,
   HTREEITEM hti
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns:

| Return code | Description |
|---|---|
| Checked | 1 |
| Unchecked | 0 |
| No Check Box Image | -1 |

## -description

Gets the check state of the specified item. You can also use the <a href="/windows/desktop/Controls/tvm-getitemstate">TVM_GETITEMSTATE</a> message directly.

## -parameters

### -param hwndTV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hti

Type: <b>HTREEITEM</b>

Handle to the item.

## -remarks

A tree-view control can have two image lists. The normal image list stores the selected, nonselected, and overlay images. Check boxes are stored in the state image list and displayed to the left of the corresponding normal image. State images are specified by a one-based index. An index of zero indicates that there is no state image. See <a href="/windows/desktop/Controls/tree-view-controls">Tree-View Image Lists</a> for a discussion of how to handle tree-view images. 

If you want to define your own state images, this macro assumes that the checked and unchecked images have the same indexes as the standard image list: 1 for unchecked and 2 for checked.
