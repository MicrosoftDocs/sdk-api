---
UID: NF:commctrl.TreeView_GetItem
title: TreeView_GetItem macro
author: windows-sdk-content
description: Retrieves some or all of a tree-view item's attributes. You can use this macro or send the TVM_GETITEM message explicitly.
old-location: controls\TreeView_GetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TreeView_GetItem, TreeView_GetItem macro [Windows Controls], _win32_TreeView_GetItem, _win32_TreeView_GetItem_cpp, commctrl/TreeView_GetItem, controls.TreeView_GetItem, controls._win32_TreeView_GetItem
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
 - TreeView_GetItem
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
- TreeView_GetItem
: 
---

# TreeView_GetItem macro


## -description


Retrieves some or all of a tree-view item's attributes. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773596(v=VS.85).aspx">TVM_GETITEM</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


### -param pitem

Type: <b>LPTVITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> structure that specifies the information to retrieve and receives information about the item. With <a href="https://msdn.microsoft.com/en-us/library/Hh298349(v=VS.85).aspx">version 4.71</a> and later, you can use a <a href="https://msdn.microsoft.com/en-us/library/Bb773459(v=VS.85).aspx">TVITEMEX</a> structure instead. 


## -remarks



When the <a href="https://msdn.microsoft.com/en-us/library/Bb773596(v=VS.85).aspx">TVM_GETITEM</a> message is sent, the 
				<b>hItem</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb773459(v=VS.85).aspx">TVITEMEX</a> structure identifies the item to retrieve information about, and the <b>mask</b> member specifies the attributes to retrieve.

If the TVIF_TEXT flag is set in the 
				<b>mask</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb773459(v=VS.85).aspx">TVITEMEX</a> structure, the <b>pszText</b> member must point to a valid buffer and the <b>cchTextMax</b> member must be set to the number of characters in that buffer. The returned text will not necessarily be stored in the original buffer passed by the application. It is possible that <b>pszText</b> will point to text in a new buffer rather than place it in the old buffer. 



