---
UID: NF:commctrl.TreeView_GetLastVisible
title: TreeView_GetLastVisible macro (commctrl.h)
description: Retrieves the last expanded item in a tree-view control. This does not retrieve the last item visible in the tree-view window. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_LASTVISIBLE flag.
helpviewer_keywords: ["TreeView_GetLastVisible","TreeView_GetLastVisible macro [Windows Controls]","_win32_TreeView_GetLastVisible","_win32_TreeView_GetLastVisible_cpp","commctrl/TreeView_GetLastVisible","controls.TreeView_GetLastVisible","controls._win32_TreeView_GetLastVisible"]
old-location: controls\TreeView_GetLastVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getlastvisible.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetLastVisible, TreeView_GetLastVisible macro [Windows Controls], _win32_TreeView_GetLastVisible, _win32_TreeView_GetLastVisible_cpp, commctrl/TreeView_GetLastVisible, controls.TreeView_GetLastVisible, controls._win32_TreeView_GetLastVisible
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
 - TreeView_GetLastVisible
 - commctrl/TreeView_GetLastVisible
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
 - TreeView_GetLastVisible
---

# TreeView_GetLastVisible macro

## -syntax

```cpp
HTREEITEM TreeView_GetLastVisible(
   HWND hwnd
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the item if successful, or <b>NULL</b> otherwise.


## -description

Retrieves the last expanded item in a tree-view control. This does not retrieve the last item visible in the tree-view window. You can use this macro, or you can explicitly send the <a href="/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_LASTVISIBLE flag.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/Controls/tvm-getitemrect">TVM_GETITEMRECT</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getfirstvisible">TreeView_GetFirstVisible</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextvisible">TreeView_GetNextVisible</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getprevvisible">TreeView_GetPrevVisible</a>
