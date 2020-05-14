---
UID: NF:commctrl.TreeView_SelectItem
title: TreeView_SelectItem macro (commctrl.h)
description: Selects the specified tree-view item. You can use this macro or the TreeView_Select macro, or you can send the TVM_SELECTITEM message explicitly.helpviewer_keywords: ["TreeView_SelectItem","TreeView_SelectItem macro [Windows Controls]","_win32_TreeView_SelectItem","_win32_TreeView_SelectItem_cpp","commctrl/TreeView_SelectItem","controls.TreeView_SelectItem","controls._win32_TreeView_SelectItem"]
old-location: controls\TreeView_SelectItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_selectitem.htm
ms.date: 12/05/2018
ms.keywords: TreeView_SelectItem, TreeView_SelectItem macro [Windows Controls], _win32_TreeView_SelectItem, _win32_TreeView_SelectItem_cpp, commctrl/TreeView_SelectItem, controls.TreeView_SelectItem, controls._win32_TreeView_SelectItem
f1_keywords:
- commctrl/TreeView_SelectItem
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
- TreeView_SelectItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_SelectItem macro


## -description


Selects the specified tree-view item. You can use this macro or the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_select">TreeView_Select</a> macro, or you can send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-selectitem">TVM_SELECTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item. 


## -remarks



When you call the <b>TreeView_SelectItem</b> macro, the control's parent window receives the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-selchanging">TVN_SELCHANGING</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-selchanged">TVN_SELCHANGED</a> notification codes. Also, if the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a> notification codes. 

Using the <b>TreeView_SelectItem</b> macro is equivalent to sending the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-selectitem">TVM_SELECTITEM</a> message with its <i>flag</i> parameter set to the TVGN_CARET value. 



