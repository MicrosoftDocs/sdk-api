---
UID: NF:commctrl.TreeView_SortChildrenCB
title: TreeView_SortChildrenCB macro
author: windows-sdk-content
description: Sorts tree-view items using an application-defined callback function that compares the items. You can use this macro or send the TVM_SORTCHILDRENCB message explicitly.
old-location: controls\TreeView_SortChildrenCB.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_sortchildrencb.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeView_SortChildrenCB, TreeView_SortChildrenCB macro [Windows Controls], _win32_TreeView_SortChildrenCB, _win32_TreeView_SortChildrenCB_cpp, commctrl/TreeView_SortChildrenCB, controls.TreeView_SortChildrenCB, controls._win32_TreeView_SortChildrenCB
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
 - TreeView_SortChildrenCB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SortChildrenCB macro


## -description


Sorts tree-view items using an application-defined callback function that compares the items. You can use this macro or send the <a href="https://msdn.microsoft.com/1669e576-5e57-49f6-8097-7d6547306014">TVM_SORTCHILDRENCB</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param psort

Type: <b>LPTVSORTCB</b>

Pointer to a <a href="https://msdn.microsoft.com/e6334b6e-d892-46fb-a225-cd779680e65d">TVSORTCB</a> structure. The <b>lpfnCompare</b> member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared. For more information about the callback function, see the description of <b>TVSORTCB</b>. 


### -param recurse

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Reserved. Must be zero. 

