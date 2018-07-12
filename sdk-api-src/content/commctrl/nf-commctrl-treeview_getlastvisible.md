---
UID: NF:commctrl.TreeView_GetLastVisible
title: TreeView_GetLastVisible macro
author: windows-sdk-content
description: Retrieves the last expanded item in a tree-view control. This does not retrieve the last item visible in the tree-view window. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_LASTVISIBLE flag.
old-location: controls\TreeView_GetLastVisible.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getlastvisible.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: TreeView_GetLastVisible, TreeView_GetLastVisible macro [Windows Controls], _win32_TreeView_GetLastVisible, _win32_TreeView_GetLastVisible_cpp, commctrl/TreeView_GetLastVisible, controls.TreeView_GetLastVisible, controls._win32_TreeView_GetLastVisible
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
 - TreeView_GetLastVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetLastVisible macro


## -description


Retrieves the last expanded item in a tree-view control. This does not retrieve the last item visible in the tree-view window. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/library/Bb773622(v=VS.85).aspx">TVM_GETNEXTITEM</a> message with the TVGN_LASTVISIBLE flag. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb773610(v=VS.85).aspx">TVM_GETITEMRECT</a>



<a href="https://msdn.microsoft.com/library/Bb773827(v=VS.85).aspx">TreeView_GetFirstVisible</a>



<a href="https://msdn.microsoft.com/library/Bb773870(v=VS.85).aspx">TreeView_GetNextVisible</a>



<a href="https://msdn.microsoft.com/library/Bb773878(v=VS.85).aspx">TreeView_GetPrevVisible</a>
 

 

