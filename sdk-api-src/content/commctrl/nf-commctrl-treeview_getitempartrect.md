---
UID: NF:commctrl.TreeView_GetItemPartRect
title: TreeView_GetItemPartRect macro
author: windows-driver-content
description: Retrieves the largest possible bounding rectangle that constitutes the &#0034;hit zone&#0034; for a specified part of an item. Use this macro or send the TVM_GETITEMPARTRECT message explicitly.
old-location: controls\TreeView_GetItemPartRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitempartrect.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: TreeView_GetItemPartRect, TreeView_GetItemPartRect macro [Windows Controls], _shell_TreeView_GetItemPartRect, _shell_TreeView_GetItemPartRect_cpp, commctrl/TreeView_GetItemPartRect, controls.TreeView_GetItemPartRect, controls._shell_TreeView_GetItemPartRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_GetItemPartRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetItemPartRect macro


## -description


Retrieves the largest possible bounding rectangle that constitutes the "hit zone" for a specified part of an item. Use this macro or send the <a href="https://msdn.microsoft.com/4fa5d167-9649-4346-89c2-8a48e8d4d2f6">TVM_GETITEMPARTRECT</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control.


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the tree-view item. 


### -param prc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the bounding rectangle. The caller is responsible for allocating this structure. The coordinates received are relative to the upper-left corner of the tree-view control.


### -param partid

Type: <b>TVITEMPART*</b>

ID of the item part. This value must be <b>TVGIPR_BUTTON</b> (0x0001).


## -remarks



This message returns the largest possible bounding rectangle such that for every (x,y) coordinate within the rectangle, a click by the user at that coordinate would constitute a hit on that part of the item.



