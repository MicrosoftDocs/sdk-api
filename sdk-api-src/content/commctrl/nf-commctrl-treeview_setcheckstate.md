---
UID: NF:commctrl.TreeView_SetCheckState
title: TreeView_SetCheckState macro (commctrl.h)
description: Sets the item's state image to &quot;checked&quot; or &quot;unchecked.&quot; You can also use the TVM_SETITEM message directly.
helpviewer_keywords: ["TreeView_SetCheckState","TreeView_SetCheckState macro [Windows Controls]","_win32_TreeView_SetCheckState","_win32_TreeView_SetCheckState_cpp","commctrl/TreeView_SetCheckState","controls.TreeView_SetCheckState","controls._win32_TreeView_SetCheckState"]
old-location: controls\TreeView_SetCheckState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setcheckstate.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetCheckState, TreeView_SetCheckState macro [Windows Controls], _win32_TreeView_SetCheckState, _win32_TreeView_SetCheckState_cpp, commctrl/TreeView_SetCheckState, controls.TreeView_SetCheckState, controls._win32_TreeView_SetCheckState
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
 - TreeView_SetCheckState
 - commctrl/TreeView_SetCheckState
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
 - TreeView_SetCheckState
---

# TreeView_SetCheckState macro

## -syntax

```cpp
UINT TreeView_SetCheckState(
   HWND      hwndTV,
   HTREEITEM hti,
   BOOL      fCheck
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The return value is not used.


## -description

Sets the item's state image to "checked" or "unchecked." You can also use the <a href="/windows/desktop/Controls/tvm-setitem">TVM_SETITEM</a> message directly.

## -parameters

### -param hwndTV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hti

Type: <b>HTREEITEM</b>

Handle to the item.

### -param fCheck

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Value that indicates which state image is displayed. Set 
					<i>fCheck</i> to <b>TRUE</b> to display the checked state image or <b>FALSE</b> to display the unchecked image.

## -remarks

A tree-view control can have two image lists. The normal image list stores the selected, nonselected, and overlay images. Check boxes are stored in the state image list and displayed to the left of the corresponding normal image. State images are specified by a one-based index. An index of zero indicates that there is no state image. See <a href="/windows/desktop/Controls/tree-view-controls">Tree-View Image Lists</a> for a discussion of how to handle tree-view images.

If you want to define your own state images, this macro assumes that the checked and unchecked images have the same indexes as the standard image list: 1 for unchecked and 2 for checked.
