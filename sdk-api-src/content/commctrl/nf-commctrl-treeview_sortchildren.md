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

# TreeView_SortChildren macro


## -description


Sorts the child items of the specified parent item in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/c18bcd5f-c083-46ee-873b-d3100b0d7b04">TVM_SORTCHILDREN</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the parent item whose child items are to be sorted. 


### -param recurse

TBD






#### - fRecurse

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value that specifies whether the sorting is recursive. Set <i>fRecurse</i> to <b>TRUE</b> to sort all levels of child items below the parent item. Otherwise, only the parent's immediate children are sorted. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks




		This message alphabetizes the tree items using <a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a> on the item name. You can use the <a href="https://msdn.microsoft.com/1669e576-5e57-49f6-8097-7d6547306014">TVM_SORTCHILDRENCB</a> message to customize the ordering behavior.
		



