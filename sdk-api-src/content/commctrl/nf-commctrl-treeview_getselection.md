---
UID: NF:commctrl.TreeView_GetSelection
title: TreeView_GetSelection macro (commctrl.h)
author: windows-sdk-content
description: Retrieves the currently selected item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_CARET flag.
old-location: controls\TreeView_GetSelection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getselection.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TreeView_GetSelection, TreeView_GetSelection macro [Windows Controls], _win32_TreeView_GetSelection, _win32_TreeView_GetSelection_cpp, commctrl/TreeView_GetSelection, controls.TreeView_GetSelection, controls._win32_TreeView_GetSelection
ms.topic: macro
f1_keywords: 
 - "commctrl/TreeView_GetSelection"
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
 - TreeView_GetSelection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetSelection macro


## -description


Retrieves the currently selected item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_CARET flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getnextitem">TreeView_GetNextItem</a>
 

 

