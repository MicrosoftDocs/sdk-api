---
UID: NF:commctrl.TreeView_GetVisibleCount
title: TreeView_GetVisibleCount macro (commctrl.h)
author: windows-sdk-content
description: Obtains the number of items that can be fully visible in the client window of a tree-view control. You can use this macro or send the TVM_GETVISIBLECOUNT message explicitly.
old-location: controls\TreeView_GetVisibleCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getvisiblecount.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TreeView_GetVisibleCount, TreeView_GetVisibleCount macro [Windows Controls], _win32_TreeView_GetVisibleCount, _win32_TreeView_GetVisibleCount_cpp, commctrl/TreeView_GetVisibleCount, controls.TreeView_GetVisibleCount, controls._win32_TreeView_GetVisibleCount
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
 - TreeView_GetVisibleCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetVisibleCount macro


## -description


Obtains the number of items that can be fully visible in the client window of a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773731(v=VS.85).aspx">TVM_GETVISIBLECOUNT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The number of items that can be fully visible may be greater than the number of items in the control. The control calculates this value by dividing the height of the client window by the height of an item. 

Note that the return value is the number of items that can be 
				<i>fully</i> visible. If you can see all of 20 items and part of one more item, the return value is 20. 



