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

# TreeView_SortChildrenCB macro


## -description


Sorts tree-view items using an application-defined callback function that compares the items. You can use this macro or send the <a href="https://msdn.microsoft.com/1669e576-5e57-49f6-8097-7d6547306014">TVM_SORTCHILDRENCB</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param psort

Type: <b>LPTVSORTCB</b>

Pointer to a <a href="https://msdn.microsoft.com/e6334b6e-d892-46fb-a225-cd779680e65d">TVSORTCB</a> structure. The <b>lpfnCompare</b> member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared. For more information about the callback function, see the description of <b>TVSORTCB</b>. 


### -param recurse

TBD






#### - fRecurse

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Reserved. Must be zero. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 

