---
UID: NF:commctrl.TreeView_EditLabel
title: TreeView_EditLabel macro
author: windows-sdk-content
description: Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.
old-location: controls\TreeView_EditLabel.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_editlabel.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeView_EditLabel, TreeView_EditLabel macro [Windows Controls], _win32_TreeView_EditLabel, _win32_TreeView_EditLabel_cpp, commctrl/TreeView_EditLabel, controls.TreeView_EditLabel, controls._win32_TreeView_EditLabel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_EditLabel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_EditLabel macro


## -description


Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text. This macro implicitly selects and focuses the specified item. You can use this macro or send the <a href="https://msdn.microsoft.com/ae844cbf-fa43-4f91-90cc-688f44bf77a5">TVM_EDITLABEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the item to edit. 


## -remarks



This macro sends a <a href="https://msdn.microsoft.com/67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44">TVN_BEGINLABELEDIT</a> notification code to the parent of the tree-view control. 

When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but do not destroy it. 

The control must have the focus before you call this macro. Focus can be set using the <a href="https://msdn.microsoft.com/88fc2959-007a-441d-8a02-19d775f28de9">SetFocus</a> function. 



