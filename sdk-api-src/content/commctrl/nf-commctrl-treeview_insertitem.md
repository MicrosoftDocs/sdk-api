---
UID: NF:commctrl.TreeView_InsertItem
title: TreeView_InsertItem macro
author: windows-sdk-content
description: Inserts a new item in a tree-view control. You can use this macro or send the TVM_INSERTITEM message explicitly.
old-location: controls\TreeView_InsertItem.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_insertitem.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: TreeView_InsertItem, TreeView_InsertItem macro [Windows Controls], _win32_TreeView_InsertItem, _win32_TreeView_InsertItem_cpp, commctrl/TreeView_InsertItem, controls.TreeView_InsertItem, controls._win32_TreeView_InsertItem
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
 - TreeView_InsertItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_InsertItem macro


## -description


Inserts a new item in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb773733(v=VS.85).aspx">TVM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param lpis

Type: <b>LPTVINSERTSTRUCT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/Bb773452(v=VS.85).aspx">TVINSERTSTRUCT</a> structure that specifies the attributes of the tree-view item. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<a href="https://msdn.microsoft.com/library/Bb773515(v=VS.85).aspx">TVN_ENDLABELEDIT</a>
 

 

