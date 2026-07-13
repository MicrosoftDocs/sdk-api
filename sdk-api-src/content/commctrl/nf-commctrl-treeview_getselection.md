---
UID: NF:commctrl.TreeView_GetSelection
title: TreeView_GetSelection macro (commctrl.h)
description: Retrieves the currently selected item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_CARET flag.
helpviewer_keywords: ["TreeView_GetSelection","TreeView_GetSelection macro [Windows Controls]","_win32_TreeView_GetSelection","_win32_TreeView_GetSelection_cpp","commctrl/TreeView_GetSelection","controls.TreeView_GetSelection","controls._win32_TreeView_GetSelection"]
old-location: controls\TreeView_GetSelection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getselection.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetSelection, TreeView_GetSelection macro [Windows Controls], _win32_TreeView_GetSelection, _win32_TreeView_GetSelection_cpp, commctrl/TreeView_GetSelection, controls.TreeView_GetSelection, controls._win32_TreeView_GetSelection
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
 - TreeView_GetSelection
 - commctrl/TreeView_GetSelection
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
 - TreeView_GetSelection
---

# TreeView_GetSelection macro

## -syntax

```cpp
HTREEITEM TreeView_GetSelection(
   HWND hwnd
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the item if successful, or <b>NULL</b> otherwise.


## -description

Retrieves the currently selected item in a tree-view control. You can use this macro, or you can explicitly send the <a href="/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_CARET flag.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextitem">TreeView_GetNextItem</a>
