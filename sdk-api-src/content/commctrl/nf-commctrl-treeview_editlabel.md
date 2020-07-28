---
UID: NF:commctrl.TreeView_EditLabel
title: TreeView_EditLabel macro (commctrl.h)
description: Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.
helpviewer_keywords: ["TreeView_EditLabel","TreeView_EditLabel macro [Windows Controls]","_win32_TreeView_EditLabel","_win32_TreeView_EditLabel_cpp","commctrl/TreeView_EditLabel","controls.TreeView_EditLabel","controls._win32_TreeView_EditLabel"]
old-location: controls\TreeView_EditLabel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_editlabel.htm
ms.date: 12/05/2018
ms.keywords: TreeView_EditLabel, TreeView_EditLabel macro [Windows Controls], _win32_TreeView_EditLabel, _win32_TreeView_EditLabel_cpp, commctrl/TreeView_EditLabel, controls.TreeView_EditLabel, controls._win32_TreeView_EditLabel
f1_keywords:
- commctrl/TreeView_EditLabel
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
- TreeView_EditLabel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_EditLabel macro


## -description


Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text. This macro implicitly selects and focuses the specified item. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-editlabel">TVM_EDITLABEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the item to edit. 


## -remarks



This macro sends a <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-beginlabeledit">TVN_BEGINLABELEDIT</a> notification code to the parent of the tree-view control. 

When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but do not destroy it. 

The control must have the focus before you call this macro. Focus can be set using the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setfocus">SetFocus</a> function. 



