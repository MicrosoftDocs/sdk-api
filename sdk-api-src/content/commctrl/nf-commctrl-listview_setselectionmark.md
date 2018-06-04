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

# ListView_SetSelectionMark macro


## -description


Sets the selection mark in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/3218f1b3-b934-4083-aaaa-e10ef1dbb6bd">LVM_SETSELECTIONMARK</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param i

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - iIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

the zero-based index of the list-view item to be selected. 


## -remarks



The selection mark is the item index from which a multiple selection starts. This macro does not affect the selection state of the item. 




## -see-also




<a href="https://msdn.microsoft.com/dba2484c-c938-4123-be28-35a504dd9e5a">ListView_GetSelectionMark</a>
 

 

