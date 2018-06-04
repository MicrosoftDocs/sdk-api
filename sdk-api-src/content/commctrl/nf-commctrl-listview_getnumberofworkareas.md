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

# ListView_GetNumberOfWorkAreas macro


## -description


Gets the number of working areas in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/ce0bcccd-62a2-45a4-959e-9959c9ca0c46">LVM_GETNUMBEROFWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param pnWorkAreas

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - lpuWorkAreas

Type: <b>LPUINT</b>

A pointer to a UINT value that receives the number of working areas in the list-view control. If zero is placed in this variable, then no working areas are currently set. This value cannot be <b>NULL</b>. 


## -see-also




<a href="https://msdn.microsoft.com/6953cdfc-8c59-4c6d-8998-f828cea3a315">Using List-View Controls</a>
 

 

