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

# GetTypeByNameW function


## -description



			The 
<b>GetTypeByName</b> function retrieves a service type <b>GUID</b> for a network service specified by name.


<div class="alert"><b>Note</b>  The 
<b>GetTypeByName</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, this reference material is included. The functions detailed in 
<a href="https://msdn.microsoft.com/f55219b9-1518-4b49-a0da-6a3fa025cca3">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2.</div>
<div> </div>



## -parameters




### -param lpServiceName [in]

A pointer to a zero-terminated string that uniquely represents the name of the service. For example, "MY SNA SERVER."


### -param lpServiceType [in, out]

A pointer to a variable to receive a globally unique identifier (<b>GUID</b>) that specifies the type of the network service. The <i>Svcguid.h</i> header file includes definitions of several <b>GUID</b> service types and macros for working with them.

The <i>Svcguid.h</i> header file is not automatically included by the <i>Winsock2.h</i> header file.


## -returns




						If the function succeeds, the return value is zero.

If the function fails, the return value is SOCKET_ERROR( – 1). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which returns the following extended error value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified service type is unknown.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74d747f0-5f5e-4f54-8b2f-7ea96d4043ee">GetNameByType</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

