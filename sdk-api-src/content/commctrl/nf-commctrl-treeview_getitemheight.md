---
UID: NF:commctrl.TreeView_GetItemHeight
title: TreeView_GetItemHeight macro (commctrl.h)
description: Retrieves the current height of the tree-view items. You can use this macro or send the TVM_GETITEMHEIGHT message explicitly.
helpviewer_keywords: ["TreeView_GetItemHeight","TreeView_GetItemHeight macro [Windows Controls]","_win32_TreeView_GetItemHeight","_win32_TreeView_GetItemHeight_cpp","commctrl/TreeView_GetItemHeight","controls.TreeView_GetItemHeight","controls._win32_TreeView_GetItemHeight"]
old-location: controls\TreeView_GetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitemheight.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetItemHeight, TreeView_GetItemHeight macro [Windows Controls], _win32_TreeView_GetItemHeight, _win32_TreeView_GetItemHeight_cpp, commctrl/TreeView_GetItemHeight, controls.TreeView_GetItemHeight, controls._win32_TreeView_GetItemHeight
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
 - TreeView_GetItemHeight
 - commctrl/TreeView_GetItemHeight
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
 - TreeView_GetItemHeight
---

# TreeView_GetItemHeight macro

## -syntax

```cpp
int TreeView_GetItemHeight(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the height of the items, in pixels.


## -description

Retrieves the current height of the tree-view items. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getitemheight">TVM_GETITEMHEIGHT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_setitemheight">TreeView_SetItemHeight</a>
