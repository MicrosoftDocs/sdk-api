---
UID: NF:commctrl.TreeView_GetCheckState
title: TreeView_GetCheckState macro
author: windows-sdk-content
description: Gets the check state of the specified item. You can also use the TVM_GETITEMSTATE message directly.
old-location: controls\TreeView_GetCheckState.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getcheckstate.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: TreeView_GetCheckState, TreeView_GetCheckState macro [Windows Controls], _win32_TreeView_GetCheckState, _win32_TreeView_GetCheckState_cpp, commctrl/TreeView_GetCheckState, controls.TreeView_GetCheckState, controls._win32_TreeView_GetCheckState
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_GetCheckState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetCheckState macro


## -description


Gets the check state of the specified item. You can also use the <a href="https://msdn.microsoft.com/89aaaa82-2809-4e4e-a325-5666a57c5cbb">TVM_GETITEMSTATE</a> message directly. 


## -parameters




### -param hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hti

TBD






#### - hItem

Type: <b>HTREEITEM</b>

Handle to the item. 


## -remarks



A tree-view control can have two image lists. The normal image list stores the selected, nonselected, and overlay images. Check boxes are stored in the state image list and displayed to the left of the corresponding normal image. State images are specified by a one-based index. An index of zero indicates that there is no state image. See <a href="Tree_View_Controls.htm">Tree-View Image Lists</a> for a discussion of how to handle tree-view images. 

If you want to define your own state images, this macro assumes that the checked and unchecked images have the same indexes as the standard image list: 1 for unchecked and 2 for checked. 



