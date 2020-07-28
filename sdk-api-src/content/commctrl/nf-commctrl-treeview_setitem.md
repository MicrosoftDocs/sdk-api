---
UID: NF:commctrl.TreeView_SetItem
title: TreeView_SetItem macro (commctrl.h)
description: The TreeView_SetItem macro sets some or all of a tree-view item's attributes. You can use this macro or send the TVM_SETITEM message explicitly.
helpviewer_keywords: ["TreeView_SetItem","TreeView_SetItem macro [Windows Controls]","_win32_TreeView_SetItem","_win32_TreeView_SetItem_cpp","commctrl/TreeView_SetItem","controls.TreeView_SetItem","controls._win32_TreeView_SetItem"]
old-location: controls\TreeView_SetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setitem.htm
ms.date: 12/05/2018
ms.keywords: TreeView_SetItem, TreeView_SetItem macro [Windows Controls], _win32_TreeView_SetItem, _win32_TreeView_SetItem_cpp, commctrl/TreeView_SetItem, controls.TreeView_SetItem, controls._win32_TreeView_SetItem
f1_keywords:
- commctrl/TreeView_SetItem
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
- TreeView_SetItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_SetItem macro


## -description


The <b>TreeView_SetItem</b> macro sets some or all of a tree-view item's attributes. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-setitem">TVM_SETITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param pitem

Type: <b>LPTVITEM</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure that contains the new item attributes. With <a href="https://docs.microsoft.com/windows/desktop/Controls/common-control-versions">version 4.71</a> and later, you can instead use a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a> structure. 


## -remarks



The <b>hItem</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> or <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a> structure identifies the item, and the <b>mask</b> member specifies which attributes to set.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getitem">TreeView_GetItem</a>
 

 

