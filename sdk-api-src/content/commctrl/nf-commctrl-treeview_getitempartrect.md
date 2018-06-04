---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



