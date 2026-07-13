---
UID: NF:commctrl.TreeView_GetNextSibling
title: TreeView_GetNextSibling macro (commctrl.h)
description: Retrieves the next sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_NEXT flag.
helpviewer_keywords: ["TreeView_GetNextSibling","TreeView_GetNextSibling macro [Windows Controls]","_win32_TreeView_GetNextSibling","_win32_TreeView_GetNextSibling_cpp","commctrl/TreeView_GetNextSibling","controls.TreeView_GetNextSibling","controls._win32_TreeView_GetNextSibling"]
old-location: controls\TreeView_GetNextSibling.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getnextsibling.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetNextSibling, TreeView_GetNextSibling macro [Windows Controls], _win32_TreeView_GetNextSibling, _win32_TreeView_GetNextSibling_cpp, commctrl/TreeView_GetNextSibling, controls.TreeView_GetNextSibling, controls._win32_TreeView_GetNextSibling
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
 - TreeView_GetNextSibling
 - commctrl/TreeView_GetNextSibling
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
 - TreeView_GetNextSibling
---

# TreeView_GetNextSibling macro

## -syntax

```cpp
HTREEITEM TreeView_GetNextSibling(
   HWND      hwnd,
   HTREEITEM hitem
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the item if successful, or <b>NULL</b> otherwise.


## -description

Retrieves the next sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_NEXT flag.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getchild">TreeView_GetChild</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextitem">TreeView_GetNextItem</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getparent">TreeView_GetParent</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getprevsibling">TreeView_GetPrevSibling</a>
