---
UID: NF:commctrl.TreeView_GetNextVisible
title: TreeView_GetNextVisible macro
author: windows-sdk-content
description: Retrieves the next visible item that follows a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_NEXTVISIBLE flag.
old-location: controls\TreeView_GetNextVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getnextvisible.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TreeView_GetNextVisible, TreeView_GetNextVisible macro [Windows Controls], _win32_TreeView_GetNextVisible, _win32_TreeView_GetNextVisible_cpp, commctrl/TreeView_GetNextVisible, controls.TreeView_GetNextVisible, controls._win32_TreeView_GetNextVisible
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
 - TreeView_GetNextVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetNextVisible macro


## -description


Retrieves the next visible item that follows a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/505c713c-7728-4119-bc0e-482fe7e73193">TVM_GETNEXTITEM</a> message with the TVGN_NEXTVISIBLE flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. The specified item must be visible. Use the <a href="https://msdn.microsoft.com/f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c">TVM_GETITEMRECT</a> message to determine whether an item is visible. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/9da74062-e029-4c73-821f-829a0964afba">TreeView_GetFirstVisible</a>



<a href="https://msdn.microsoft.com/987d0d0f-eecf-4a6a-9340-64dd6ce1ac80">TreeView_GetNextItem</a>



<a href="https://msdn.microsoft.com/b9a4ad11-bd4a-48c6-9dbb-a92a3e410dc3">TreeView_GetPrevVisible</a>
 

 

