---
UID: NF:commctrl.TreeView_EnsureVisible
title: TreeView_EnsureVisible macro (commctrl.h)

description: Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary. You can use this macro or send the TVM_ENSUREVISIBLE message explicitly.
old-location: controls\TreeView_EnsureVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_ensurevisible.htm

ms.date: 12/05/2018
ms.keywords: TreeView_EnsureVisible, TreeView_EnsureVisible macro [Windows Controls], _win32_TreeView_EnsureVisible, _win32_TreeView_EnsureVisible_cpp, commctrl/TreeView_EnsureVisible, controls.TreeView_EnsureVisible, controls._win32_TreeView_EnsureVisible
ms.topic: macro
f1_keywords: 
 - "commctrl/TreeView_EnsureVisible"
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
 - TreeView_EnsureVisible
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_EnsureVisible macro


## -description


Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-ensurevisible">TVM_ENSUREVISIBLE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the item. 


## -remarks



If the <b>TreeView_EnsureVisible</b> macro expands the parent item, the parent window receives the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a> notification codes. 



