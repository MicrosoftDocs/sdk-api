---
UID: NF:commctrl.TreeView_GetLastVisible
title: TreeView_GetLastVisible macro
author: windows-driver-content
description: Retrieves the last expanded item in a tree-view control. This does not retrieve the last item visible in the tree-view window. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_LASTVISIBLE flag.
old-location: controls\TreeView_GetLastVisible.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getlastvisible.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: TreeView_GetLastVisible, TreeView_GetLastVisible macro [Windows Controls], _win32_TreeView_GetLastVisible, _win32_TreeView_GetLastVisible_cpp, commctrl/TreeView_GetLastVisible, controls.TreeView_GetLastVisible, controls._win32_TreeView_GetLastVisible
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
-	TreeView_GetLastVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetLastVisible macro


## -description


Retrieves the last expanded item in a tree-view control. This does not retrieve the last item visible in the tree-view window. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/505c713c-7728-4119-bc0e-482fe7e73193">TVM_GETNEXTITEM</a> message with the TVGN_LASTVISIBLE flag. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c">TVM_GETITEMRECT</a>



<a href="https://msdn.microsoft.com/9da74062-e029-4c73-821f-829a0964afba">TreeView_GetFirstVisible</a>



<a href="https://msdn.microsoft.com/7e21cd1b-d05e-4c62-9ec8-244a096f90f3">TreeView_GetNextVisible</a>



<a href="https://msdn.microsoft.com/b9a4ad11-bd4a-48c6-9dbb-a92a3e410dc3">TreeView_GetPrevVisible</a>
 

 

