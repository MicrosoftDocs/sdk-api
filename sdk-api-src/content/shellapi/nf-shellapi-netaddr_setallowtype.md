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

# NetAddr_SetAllowType macro


## -description


Sets the network address types that a specified network address control accepts.


## -parameters




### -param hwnd [in]

A handle to the network address control.


### -param addrMask [in]

Specifies the network address types as one or more of the <a href="https://msdn.microsoft.com/4144dac9-772c-49cb-b924-e852fb4c81c7">NET_STRING</a> constants.
                


## -remarks



The mask set is the criterion used to validate a network address in the macro <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a>.

Use this macro for a network address control only. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="https://msdn.microsoft.com/52b475e3-7335-4c34-80d7-ccd81af0e0ec">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.




## -see-also




<a href="https://msdn.microsoft.com/21533513-86c2-418b-ab62-3c1b2db9bc2f">NetAddr_GetAllowType</a>
 

 

