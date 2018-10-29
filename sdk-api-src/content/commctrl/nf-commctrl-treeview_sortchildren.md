---
UID: NF:commctrl.TreeView_SortChildren
title: TreeView_SortChildren macro
author: windows-sdk-content
description: Sorts the child items of the specified parent item in a tree-view control. You can use this macro or send the TVM_SORTCHILDREN message explicitly.
old-location: controls\TreeView_SortChildren.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_sortchildren.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TreeView_SortChildren, TreeView_SortChildren macro [Windows Controls], _win32_TreeView_SortChildren, _win32_TreeView_SortChildren_cpp, commctrl/TreeView_SortChildren, controls.TreeView_SortChildren, controls._win32_TreeView_SortChildren
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
 - TreeView_SortChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SortChildren macro


## -description


Sorts the child items of the specified parent item in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/c18bcd5f-c083-46ee-873b-d3100b0d7b04">TVM_SORTCHILDREN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the parent item whose child items are to be sorted. 


### -param recurse

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value that specifies whether the sorting is recursive. Set <i>fRecurse</i> to <b>TRUE</b> to sort all levels of child items below the parent item. Otherwise, only the parent's immediate children are sorted. 


## -remarks



This message alphabetizes the tree items using <a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a> on the item name. You can use the <a href="https://msdn.microsoft.com/1669e576-5e57-49f6-8097-7d6547306014">TVM_SORTCHILDRENCB</a> message to customize the ordering behavior.
		



