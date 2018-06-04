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

# GetNameByTypeA function


## -description


The 
<b>GetNameByType</b> function retrieves the name of a network service for the specified service type.


<div class="alert"><b>Note</b>  The 
<b>GetNameByType</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, the reference material is as follows.</div>
<div> </div>



<div class="alert"><b>Note</b>  The functions detailed in 
<a href="https://msdn.microsoft.com/f55219b9-1518-4b49-a0da-6a3fa025cca3">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2.</div>
<div> </div>



## -parameters




### -param lpServiceType [in]

A pointer to a globally unique identifier (GUID) that specifies the type of the network service. The <i>Svcguid.h</i> header file includes definitions of several GUID service types, and macros for working with them.

The <i>Svcguid.h</i> header file is not automatically included by the <i>Winsock2.h</i> header file.


### -param lpServiceName [out]

A pointer to a buffer to receive a zero-terminated string that uniquely represents the name of the network service.


### -param dwNameLength [in]

A pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpServiceName</i>. On output, the variable contains the actual size of the service name string, in bytes.


## -returns



If the function succeeds, the return value is not SOCKET_ERROR (–1).

If the function fails, the return value is SOCKET_ERROR (–1). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/177bbae5-bc00-4ce5-a0f7-8474f0c2cb2e">GetTypeByName</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

