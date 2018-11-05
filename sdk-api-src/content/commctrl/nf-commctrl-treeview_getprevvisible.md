---
UID: NF:commctrl.TreeView_GetPrevVisible
title: TreeView_GetPrevVisible macro
author: windows-sdk-content
description: Retrieves the first visible item that precedes a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PREVIOUSVISIBLE flag.
old-location: controls\TreeView_GetPrevVisible.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getprevvisible.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TreeView_GetPrevVisible, TreeView_GetPrevVisible macro [Windows Controls], _win32_TreeView_GetPrevVisible, _win32_TreeView_GetPrevVisible_cpp, commctrl/TreeView_GetPrevVisible, controls.TreeView_GetPrevVisible, controls._win32_TreeView_GetPrevVisible
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
 - TreeView_GetPrevVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetPrevVisible macro


## -description


Retrieves the first visible item that precedes a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/en-us/library/Bb773622(v=VS.85).aspx">TVM_GETNEXTITEM</a> message with the TVGN_PREVIOUSVISIBLE flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. The specified item must be visible. Use the <a href="https://msdn.microsoft.com/en-us/library/Bb773610(v=VS.85).aspx">TVM_GETITEMRECT</a> message to determine whether an item is visible. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773827(v=VS.85).aspx">TreeView_GetFirstVisible</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773861(v=VS.85).aspx">TreeView_GetNextItem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773870(v=VS.85).aspx">TreeView_GetNextVisible</a>
 

 

