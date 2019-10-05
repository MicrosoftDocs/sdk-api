---
UID: NF:commctrl.TreeView_GetNextSelected
title: TreeView_GetNextSelected macro (commctrl.h)
author: windows-sdk-content
description: Retrieves the tree-view item that bears the TVGN_NEXTSELECTED relationship to a specified tree item.
old-location: controls\TreeView_GetNextSelected.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getnextselected.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TreeView_GetNextSelected, TreeView_GetNextSelected macro [Windows Controls], _shell_TreeView_GetNextSelected, _shell_TreeView_GetNextSelected_cpp, commctrl/TreeView_GetNextSelected, controls.TreeView_GetNextSelected, controls._shell_TreeView_GetNextSelected
ms.topic: macro
f1_keywords: 
 - "commctrl/TreeView_GetNextSelected"
dev_langs:
 - c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - TreeView_GetNextSelected
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetNextSelected macro


## -description


Retrieves the tree-view item that bears the <b>TVGN_NEXTSELECTED</b> relationship to a specified tree item.


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.


### -param hitem

Type: <b>HTREEITEM*</b>

Specifies the tree item by handle.


## -remarks



Used to find the next selected item when there are multiple items selected.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a>
 

 

