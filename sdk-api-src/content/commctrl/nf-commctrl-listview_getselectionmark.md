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

# ListView_GetSelectionMark macro


## -description


Gets the selection mark from a list-view control. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/21daf7d7-1217-4608-93f9-c390546f1591">LVM_GETSELECTIONMARK</a> message. 


## -parameters




### -param hwnd

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


## -remarks



The selection mark is the item index from which a multiple selection starts. 




## -see-also




<a href="https://msdn.microsoft.com/75cb06d0-3d6f-4523-b912-3c12e368f17e">ListView_SetSelectionMark</a>
 

 

