---
UID: NF:commctrl.TreeView_InsertItem
title: TreeView_InsertItem macro (commctrl.h)
author: windows-sdk-content
description: Inserts a new item in a tree-view control. You can use this macro or send the TVM_INSERTITEM message explicitly.
old-location: controls\TreeView_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_insertitem.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TreeView_InsertItem, TreeView_InsertItem macro [Windows Controls], _win32_TreeView_InsertItem, _win32_TreeView_InsertItem_cpp, commctrl/TreeView_InsertItem, controls.TreeView_InsertItem, controls._win32_TreeView_InsertItem
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
 - TreeView_InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_InsertItem macro


## -description


Inserts a new item in a tree-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-insertitem">TVM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param lpis

Type: <b>LPTVINSERTSTRUCT</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tagtvinsertstructa">TVINSERTSTRUCT</a> structure that specifies the attributes of the tree-view item. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-endlabeledit">TVN_ENDLABELEDIT</a>
 

 

