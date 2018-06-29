---
UID: NF:commctrl.TreeView_DeleteItem
title: TreeView_DeleteItem macro
author: windows-sdk-content
description: Removes an item and all its children from a tree-view control. You can also send the TVM_DELETEITEM message explicitly.
old-location: controls\TreeView_DeleteItem.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_deleteitem.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: TreeView_DeleteItem, TreeView_DeleteItem macro [Windows Controls], _win32_TreeView_DeleteItem, _win32_TreeView_DeleteItem_cpp, commctrl/TreeView_DeleteItem, controls.TreeView_DeleteItem, controls._win32_TreeView_DeleteItem
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
 - TreeView_DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_DeleteItem macro


## -description


Removes an item and all its children from a tree-view control. You can also send the <a href="https://msdn.microsoft.com/library/Bb773560(v=VS.85).aspx">TVM_DELETEITEM</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

<b>HTREEITEM</b> handle to the item to delete. If <i>hitem</i> is set to TVI_ROOT, all items are deleted from the tree-view control. You can also use the <a href="https://msdn.microsoft.com/library/Bb773790(v=VS.85).aspx">TreeView_DeleteAllItems</a> macro to delete all items. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



It is not safe to delete items in response to a notification such as <a href="https://msdn.microsoft.com/library/Bb773547(v=VS.85).aspx">TVN_SELCHANGING</a>.

Once an item is deleted, its handle is invalid and cannot be used.

The parent window receives a <a href="https://msdn.microsoft.com/library/Bb773512(v=VS.85).aspx">TVN_DELETEITEM</a> notification code when each item is removed. 

If the item label is being edited, the edit operation is canceled and the parent window receives the <a href="https://msdn.microsoft.com/library/Bb773515(v=VS.85).aspx">TVN_ENDLABELEDIT</a> notification code. 

If you delete all items in a tree-view control that has the <a href="https://msdn.microsoft.com/library/Bb760013(v=VS.85).aspx">TVS_NOSCROLL</a> style, items subsequently added may not display properly. For more information, see <a href="https://msdn.microsoft.com/library/Bb773790(v=VS.85).aspx">TreeView_DeleteAllItems</a>.



