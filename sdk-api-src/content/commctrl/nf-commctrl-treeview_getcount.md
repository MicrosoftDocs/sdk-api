---
UID: NF:commctrl.TreeView_GetCount
title: TreeView_GetCount macro
author: windows-sdk-content
description: Retrieves a count of the items in a tree-view control. You can use this macro or send the TVM_GETCOUNT message explicitly.
old-location: controls\TreeView_GetCount.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getcount.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TreeView_GetCount, TreeView_GetCount macro [Windows Controls], _win32_TreeView_GetCount, _win32_TreeView_GetCount_cpp, commctrl/TreeView_GetCount, controls.TreeView_GetCount, controls._win32_TreeView_GetCount
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
 - TreeView_GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- TreeView_GetCount
: 
---

# TreeView_GetCount macro


## -description


Retrieves a count of the items in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773572(v=VS.85).aspx">TVM_GETCOUNT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The node count returned by <b>TreeView_GetCount</b> is limited to integer values. If you add a node beyond 32767 the macro returns a negative value. After adding 65536 nodes the count returns to zero. When this occurs, the tree-view control appears empty with no scrollbars. For more information see the Knowledge Base article <a href="http://go.microsoft.com/fwlink/p/?linkid=198357">Q182231</a>.
		



