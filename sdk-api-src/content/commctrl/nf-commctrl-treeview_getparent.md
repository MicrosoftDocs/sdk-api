---
UID: NF:commctrl.TreeView_GetParent
title: TreeView_GetParent macro (commctrl.h)
description: Retrieves the parent item of the specified tree-view item. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PARENT flag.
helpviewer_keywords: ["TreeView_GetParent","TreeView_GetParent macro [Windows Controls]","_win32_TreeView_GetParent","_win32_TreeView_GetParent_cpp","commctrl/TreeView_GetParent","controls.TreeView_GetParent","controls._win32_TreeView_GetParent"]
old-location: controls\TreeView_GetParent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getparent.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetParent, TreeView_GetParent macro [Windows Controls], _win32_TreeView_GetParent, _win32_TreeView_GetParent_cpp, commctrl/TreeView_GetParent, controls.TreeView_GetParent, controls._win32_TreeView_GetParent
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
 - TreeView_GetParent
 - commctrl/TreeView_GetParent
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
 - TreeView_GetParent
---

# TreeView_GetParent macro

## -syntax

```cpp
HTREEITEM TreeView_GetParent(
   HWND      hwnd,
   HTREEITEM hitem
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the item if successful. For most cases, the message returns a <b>NULL</b> value to indicate an error. See the Remarks section for details.

## -description

Retrieves the parent item of the specified tree-view item. You can use this macro, or you can explicitly send the <a href="/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_PARENT flag.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle to the parent item of this tree-view item, or NULL.

## -remarks

This macro will return <b>NULL</b> if the parent of the specified item is the root node of the tree.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getchild">TreeView_GetChild</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextitem">TreeView_GetNextItem</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextsibling">TreeView_GetNextSibling</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getprevsibling">TreeView_GetPrevSibling</a>
