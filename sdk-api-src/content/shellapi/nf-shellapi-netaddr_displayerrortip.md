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

# NetAddr_DisplayErrorTip macro


## -description


Displays an error message in the balloon tip associated with the network address control.


## -parameters




### -param hwnd [in]

A handle to the network address control.


## -remarks



Call this macro to display an error message when an address typed into the control does not validate against the allowed network address types set with macro <a href="https://msdn.microsoft.com/2fa97abd-79c8-41ce-bd0e-75941bf4d005">NetAddr_SetAllowType</a>. Use the macro <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a> to validate the address.




## -see-also




<a href="https://msdn.microsoft.com/21533513-86c2-418b-ab62-3c1b2db9bc2f">NetAddr_GetAllowType</a>
 

 

