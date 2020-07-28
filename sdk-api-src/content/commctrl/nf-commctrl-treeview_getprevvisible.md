---
UID: NF:commctrl.TreeView_GetPrevVisible
title: TreeView_GetPrevVisible macro (commctrl.h)
description: Retrieves the first visible item that precedes a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PREVIOUSVISIBLE flag.
helpviewer_keywords: ["TreeView_GetPrevVisible","TreeView_GetPrevVisible macro [Windows Controls]","_win32_TreeView_GetPrevVisible","_win32_TreeView_GetPrevVisible_cpp","commctrl/TreeView_GetPrevVisible","controls.TreeView_GetPrevVisible","controls._win32_TreeView_GetPrevVisible"]
old-location: controls\TreeView_GetPrevVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getprevvisible.htm
ms.date: 12/05/2018
ms.keywords: TreeView_GetPrevVisible, TreeView_GetPrevVisible macro [Windows Controls], _win32_TreeView_GetPrevVisible, _win32_TreeView_GetPrevVisible_cpp, commctrl/TreeView_GetPrevVisible, controls.TreeView_GetPrevVisible, controls._win32_TreeView_GetPrevVisible
f1_keywords:
- commctrl/TreeView_GetPrevVisible
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- TreeView_GetPrevVisible
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetPrevVisible macro


## -description


Retrieves the first visible item that precedes a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_PREVIOUSVISIBLE flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. The specified item must be visible. Use the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getitemrect">TVM_GETITEMRECT</a> message to determine whether an item is visible. 


## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getfirstvisible">TreeView_GetFirstVisible</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextitem">TreeView_GetNextItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextvisible">TreeView_GetNextVisible</a>
 

 

