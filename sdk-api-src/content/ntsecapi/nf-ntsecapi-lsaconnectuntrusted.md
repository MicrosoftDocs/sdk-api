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

# LsaConnectUntrusted function


## -description


The <b>LsaConnectUntrusted</b> function establishes an untrusted connection to the LSA server.


## -parameters




### -param LsaHandle [out]

Pointer to a handle that receives the connection handle, which must be provided in future authentication services.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



<b>LsaConnectUntrusted</b> returns a handle to an untrusted connection; it does not verify any information about the caller. The handle should be closed using the 
<a href="https://msdn.microsoft.com/8a956469-9538-4d71-8158-af22aa26f840">LsaDeregisterLogonProcess</a> function.

If your application simply needs to query information from authentication packages, you can use the handle returned by this function in calls to 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> and 
<a href="https://msdn.microsoft.com/c6504aea-fdba-44ac-b2dc-070707bb1183">LsaLookupAuthenticationPackage</a>.

Applications with the SeTcbPrivilege privilege may create a trusted connection by calling 
<a href="https://msdn.microsoft.com/1bef2949-b4c8-400e-8a2d-60aa88a4e238">LsaRegisterLogonProcess</a>.




## -see-also




<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>



<a href="https://msdn.microsoft.com/8a956469-9538-4d71-8158-af22aa26f840">LsaDeregisterLogonProcess</a>



<a href="https://msdn.microsoft.com/c6504aea-fdba-44ac-b2dc-070707bb1183">LsaLookupAuthenticationPackage</a>



<a href="https://msdn.microsoft.com/1bef2949-b4c8-400e-8a2d-60aa88a4e238">LsaRegisterLogonProcess</a>
 

 

