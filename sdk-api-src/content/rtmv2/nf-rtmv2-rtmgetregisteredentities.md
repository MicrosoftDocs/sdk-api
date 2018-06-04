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

# RtmGetRegisteredEntities function


## -description


The 
<b>RtmGetRegisteredEntities</b> function returns information about all clients that have registered with the specified instance of the routing table manager and specified address family.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NumEntities [in, out]

On input, <i>NumEntities</i> is a pointer to a <b>UINT</b> value, which specifies the maximum number of clients that can be received by <i>EntityInfos</i>. On output, <i>NumEntities</i> receives the actual number of clients received by <i>EntityInfos</i>.


### -param EntityHandles [out]

If handles must be returned: On input, <i>EntityHandles</i> is a pointer to <b>NULL</b>. On output, <i>EntityHandles</i> receives a pointer to an array of entity handle; otherwise, <i>EntityHandles</i> remains unchanged. 




If handles do not need to be returned: On input, <i>EntityHandles</i> is <b>NULL</b>.


### -param OPTIONAL

TBD




#### - EntityInfos [out]

If a pointer must be returned: On input, <i>EntityInfos</i> is a pointer to <b>NULL</b>. On output, <i>EntityInfos</i> receives a pointer to an array of 
<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a> structures; otherwise, <i>EntityInfos</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>EntityInfos</i> is <b>NULL</b>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer supplied is not large enough to hold all the requested information.

</td>
</tr>
</table>
 




## -remarks



If <b>ERROR_INSUFFICIENT_BUFFER</b> is returned, there may be some data in <i>EntityHandles</i>. The <i>NumEntities</i> parameter specifies how many entities were actually returned.

The 
<b>RtmGetRegisteredEntities</b> function can be used by routing protocols to verify which other protocols are running for that address family and routing table manager instance. Based on the information returned, a client can then perform protocol-specific processing.

The RTMv2 API supports only one instance of the routing table manager.

When the entities are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/1f6c4275-0129-4f27-b9b2-bfda33d34d21">RtmReleaseEntities</a>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/a96a4089-6a7c-4565-baeb-5d5fa7b84b35">Enumerate the Registered Entities</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a>



<a href="https://msdn.microsoft.com/1f6c4275-0129-4f27-b9b2-bfda33d34d21">RtmReleaseEntities</a>
 

 

