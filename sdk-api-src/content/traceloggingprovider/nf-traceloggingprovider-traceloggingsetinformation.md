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

# TraceLoggingSetInformation function


## -description


Provides special-purpose information to the Event Tracing for Windows (ETW) runtime.


## -parameters




### -param hProvider [in, out]

Handle to the provider.


### -param informationClass [in]

The type of information for the provider.


### -param pvInformation [in]

The input buffer.


### -param cbInformation [in]

The size of the input buffer.


## -returns



If you call this function from user mode code, the function returns a HRESULT. Use the SUCCEEDED() macro to determine if the function succeeds.

 If you call this function from kernel mode code, the function returns a NTSTATUS. Use the NT_SUCCESS() macro to determine if the function succeeds.




## -remarks



This function serves as a wrapper around the <a href="https://msdn.microsoft.com/e8b408ba-4bb5-4166-bf43-d18e4fe8de32">EventSetInformation</a> function.

To control the behavior of this function, use macros TLG_EVENT_SET_INFORMATION and TLG_HAVE_EVENT_SET_INFORMATION.



