---
UID: NF:commctrl.TreeView_GetPrevSibling
title: TreeView_GetPrevSibling macro (commctrl.h)
description: Retrieves the previous sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PREVIOUS flag.
helpviewer_keywords: ["TreeView_GetPrevSibling","TreeView_GetPrevSibling macro [Windows Controls]","_win32_TreeView_GetPrevSibling","_win32_TreeView_GetPrevSibling_cpp","commctrl/TreeView_GetPrevSibling","controls.TreeView_GetPrevSibling","controls._win32_TreeView_GetPrevSibling"]
old-location: controls\TreeView_GetPrevSibling.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getprevsibling.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetPrevSibling, TreeView_GetPrevSibling macro [Windows Controls], _win32_TreeView_GetPrevSibling, _win32_TreeView_GetPrevSibling_cpp, commctrl/TreeView_GetPrevSibling, controls.TreeView_GetPrevSibling, controls._win32_TreeView_GetPrevSibling
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
 - TreeView_GetPrevSibling
 - commctrl/TreeView_GetPrevSibling
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
 - TreeView_GetPrevSibling
---

# TreeView_GetPrevSibling macro

## -syntax

```cpp
HTREEITEM TreeView_GetPrevSibling(
   HWND      hwnd,
   HTREEITEM hitem
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the item if successful, or <b>NULL</b> otherwise.


## -description

Retrieves the previous sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_PREVIOUS flag.

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



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextsibling">TreeView_GetNextSibling</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getparent">TreeView_GetParent</a>
