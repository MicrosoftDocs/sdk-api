---
UID: NF:commctrl.TreeView_SetItem
title: TreeView_SetItem macro
author: windows-sdk-content
description: The TreeView_SetItem macro sets some or all of a tree-view item's attributes. You can use this macro or send the TVM_SETITEM message explicitly.
old-location: controls\TreeView_SetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TreeView_SetItem, TreeView_SetItem macro [Windows Controls], _win32_TreeView_SetItem, _win32_TreeView_SetItem_cpp, commctrl/TreeView_SetItem, controls.TreeView_SetItem, controls._win32_TreeView_SetItem
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
 - TreeView_SetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetItem macro


## -description


The <b>TreeView_SetItem</b> macro sets some or all of a tree-view item's attributes. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773758(v=VS.85).aspx">TVM_SETITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param pitem

Type: <b>LPTVITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> structure that contains the new item attributes. With <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">version 4.71</a> and later, you can instead use a <a href="https://msdn.microsoft.com/en-us/library/Bb773459(v=VS.85).aspx">TVITEMEX</a> structure. 


## -remarks



The <b>hItem</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb773459(v=VS.85).aspx">TVITEMEX</a> structure identifies the item, and the <b>mask</b> member specifies which attributes to set.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773841(v=VS.85).aspx">TreeView_GetItem</a>
 

 

