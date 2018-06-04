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

# RtmGetOpaqueInformationPointer function


## -description


The 
<b>RtmGetOpaqueInformationPointer</b> function returns a pointer to the opaque information field in a destination that is reserved for this client. The pointer enables the client to store client-specific information with the destination in the routing table.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param DestHandle [in]

Handle to the destination.


### -param OpaqueInfoPointer [out]

On input, <i>OpaqueInfoPointer</i> is a pointer to <b>NULL</b>. 




On output, <i>OpaqueInfoPointer</i> receives a pointer to the opaque information pointer. If a client has not reserved an opaque pointer during registration, this parameter remains unchanged.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No opaque pointer was reserved by the client.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



For sample code using this function, see 
<a href="https://msdn.microsoft.com/9bf420a1-2d9b-4be9-bd96-c92023b0ed41">Access the Opaque Pointer in a Destination</a>.




## -see-also




<a href="https://msdn.microsoft.com/5666dc47-811f-481e-8bda-bf814a4028de">RtmLockDestination</a>
 

 

