---
UID: NF:commctrl.TreeView_GetItemState
title: TreeView_GetItemState macro
author: windows-driver-content
description: Retrieves some or all of a tree-view item's state attributes. You can use this macro or send the TVM_GETITEMSTATE message explicitly.
old-location: controls\TreeView_GetItemState.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitemstate.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: TreeView_GetItemState, TreeView_GetItemState macro [Windows Controls], _win32_TreeView_GetItemState, _win32_TreeView_GetItemState_cpp, commctrl/TreeView_GetItemState, controls.TreeView_GetItemState, controls._win32_TreeView_GetItemState
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_GetItemState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetItemState macro


## -description


Retrieves some or all of a tree-view item's state attributes. You can use this macro or send the <a href="https://msdn.microsoft.com/89aaaa82-2809-4e4e-a325-5666a57c5cbb">TVM_GETITEMSTATE</a> message explicitly. 


## -parameters




### -param hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hti

TBD


### -param mask

TBD






#### - hItem

Type: <b>HTREEITEM</b>

Handle to the item. 


#### - stateMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Mask used to specify the states to query for. It is equivalent to the <b>stateMask</b> member of <a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a>. 

