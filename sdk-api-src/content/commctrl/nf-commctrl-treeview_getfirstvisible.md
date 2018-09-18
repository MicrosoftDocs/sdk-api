---
UID: NF:commctrl.TreeView_GetFirstVisible
title: TreeView_GetFirstVisible macro
author: windows-sdk-content
description: Retrieves the first visible item in a tree-view control window. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_FIRSTVISIBLE flag.
old-location: controls\TreeView_GetFirstVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getfirstvisible.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TreeView_GetFirstVisible, TreeView_GetFirstVisible macro [Windows Controls], _win32_TreeView_GetFirstVisible, _win32_TreeView_GetFirstVisible_cpp, commctrl/TreeView_GetFirstVisible, controls.TreeView_GetFirstVisible, controls._win32_TreeView_GetFirstVisible
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
 - TreeView_GetFirstVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetFirstVisible macro


## -description


Retrieves the first visible item in a tree-view control window. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/505c713c-7728-4119-bc0e-482fe7e73193">TVM_GETNEXTITEM</a> message with the TVGN_FIRSTVISIBLE flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c">TVM_GETITEMRECT</a>



<a href="https://msdn.microsoft.com/b46dbbff-0571-4c46-91b3-4601e1707799">TreeView_GetLastVisible</a>



<a href="https://msdn.microsoft.com/7e21cd1b-d05e-4c62-9ec8-244a096f90f3">TreeView_GetNextVisible</a>



<a href="https://msdn.microsoft.com/b9a4ad11-bd4a-48c6-9dbb-a92a3e410dc3">TreeView_GetPrevVisible</a>
 

 

