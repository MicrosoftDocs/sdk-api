---
UID: NF:commctrl.TreeView_EnsureVisible
title: TreeView_EnsureVisible macro
author: windows-driver-content
description: Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary. You can use this macro or send the TVM_ENSUREVISIBLE message explicitly.
old-location: controls\TreeView_EnsureVisible.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_ensurevisible.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: TreeView_EnsureVisible, TreeView_EnsureVisible macro [Windows Controls], _win32_TreeView_EnsureVisible, _win32_TreeView_EnsureVisible_cpp, commctrl/TreeView_EnsureVisible, controls.TreeView_EnsureVisible, controls._win32_TreeView_EnsureVisible
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
-	TreeView_EnsureVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_EnsureVisible macro


## -description


Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary. You can use this macro or send the <a href="https://msdn.microsoft.com/7053438a-f9ca-4c4c-9da6-46b99fe1e4f8">TVM_ENSUREVISIBLE</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the item. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



If the <b>TreeView_EnsureVisible</b> macro expands the parent item, the parent window receives the <a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/18d9d61d-6ec5-4d3b-9c02-36d0e61ed232">TVN_ITEMEXPANDED</a> notification codes. 



