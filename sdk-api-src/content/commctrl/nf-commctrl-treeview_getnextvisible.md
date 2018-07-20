---
UID: NF:commctrl.TreeView_GetNextVisible
title: TreeView_GetNextVisible macro
author: windows-sdk-content
description: Retrieves the next visible item that follows a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_NEXTVISIBLE flag.
old-location: controls\TreeView_GetNextVisible.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getnextvisible.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: TreeView_GetNextVisible, TreeView_GetNextVisible macro [Windows Controls], _win32_TreeView_GetNextVisible, _win32_TreeView_GetNextVisible_cpp, commctrl/TreeView_GetNextVisible, controls.TreeView_GetNextVisible, controls._win32_TreeView_GetNextVisible
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
 - TreeView_GetNextVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetNextVisible macro


## -description


Retrieves the next visible item that follows a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/library/Bb773622(v=VS.85).aspx">TVM_GETNEXTITEM</a> message with the TVGN_NEXTVISIBLE flag. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. The specified item must be visible. Use the <a href="https://msdn.microsoft.com/library/Bb773610(v=VS.85).aspx">TVM_GETITEMRECT</a> message to determine whether an item is visible. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb773827(v=VS.85).aspx">TreeView_GetFirstVisible</a>



<a href="https://msdn.microsoft.com/library/Bb773861(v=VS.85).aspx">TreeView_GetNextItem</a>



<a href="https://msdn.microsoft.com/library/Bb773878(v=VS.85).aspx">TreeView_GetPrevVisible</a>
 

 

