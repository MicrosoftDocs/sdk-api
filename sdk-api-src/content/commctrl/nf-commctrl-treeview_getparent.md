---
UID: NF:commctrl.TreeView_GetParent
title: TreeView_GetParent macro (commctrl.h)
description: Retrieves the parent item of the specified tree-view item. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PARENT flag.
old-location: controls\TreeView_GetParent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getparent.htm
ms.date: 12/05/2018
ms.keywords: TreeView_GetParent, TreeView_GetParent macro [Windows Controls], _win32_TreeView_GetParent, _win32_TreeView_GetParent_cpp, commctrl/TreeView_GetParent, controls.TreeView_GetParent, controls._win32_TreeView_GetParent
f1_keywords:
- commctrl/TreeView_GetParent
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
- TreeView_GetParent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetParent macro


## -description


Retrieves the parent item of the specified tree-view item. You can use this macro, or you can explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_PARENT flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. 


## -remarks



This macro will return <b>NULL</b> if the parent of the specified item is the root node of the tree.




## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getchild">TreeView_GetChild</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextitem">TreeView_GetNextItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextsibling">TreeView_GetNextSibling</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getprevsibling">TreeView_GetPrevSibling</a>
 

 

