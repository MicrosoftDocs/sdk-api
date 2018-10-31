---
UID: NF:commctrl.TreeView_GetDropHilight
title: TreeView_GetDropHilight macro
author: windows-sdk-content
description: Retrieves the tree-view item that is the target of a drag-and-drop operation. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_DROPHILITE flag.
old-location: controls\TreeView_GetDropHilight.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getdrophilight.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TreeView_GetDropHilight, TreeView_GetDropHilight macro [Windows Controls], _win32_TreeView_GetDropHilight, _win32_TreeView_GetDropHilight_cpp, commctrl/TreeView_GetDropHilight, controls.TreeView_GetDropHilight, controls._win32_TreeView_GetDropHilight
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
 - TreeView_GetDropHilight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetDropHilight macro


## -description


Retrieves the tree-view item that is the target of a drag-and-drop operation. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/505c713c-7728-4119-bc0e-482fe7e73193">TVM_GETNEXTITEM</a> message with the TVGN_DROPHILITE flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 

