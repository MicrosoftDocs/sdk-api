---
UID: NF:commctrl.TreeView_InsertItem
title: TreeView_InsertItem macro
author: windows-sdk-content
description: Inserts a new item in a tree-view control. You can use this macro or send the TVM_INSERTITEM message explicitly.
old-location: controls\TreeView_InsertItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_insertitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TreeView_InsertItem, TreeView_InsertItem macro [Windows Controls], _win32_TreeView_InsertItem, _win32_TreeView_InsertItem_cpp, commctrl/TreeView_InsertItem, controls.TreeView_InsertItem, controls._win32_TreeView_InsertItem
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
 - TreeView_InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_InsertItem macro


## -description


Inserts a new item in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e">TVM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param lpis

Type: <b>LPTVINSERTSTRUCT</b>

Pointer to a <a href="https://msdn.microsoft.com/ff0f4494-f41f-4e21-96e5-8e9aa9ef88bf">TVINSERTSTRUCT</a> structure that specifies the attributes of the tree-view item. 


## -see-also




<a href="https://msdn.microsoft.com/82eb9fcd-de10-4efb-8501-78c5af5e089e">TVN_ENDLABELEDIT</a>
 

 

