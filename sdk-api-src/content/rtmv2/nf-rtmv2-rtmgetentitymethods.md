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

# RtmGetEntityMethods function


## -description


The 
<b>RtmGetEntityMethods</b> function queries the specified client to determine which methods are available for another client to invoke.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EntityHandle [in]

Handle to the client for which to obtain methods.


### -param NumMethods [in, out]

On input, <i>NumMethods</i> specifies a valid pointer to a <b>UINT</b> value. Specify zero to return the number of methods available to be exported. 




On output, <i>NumMethods</i> receives the number of methods exported by the client.


### -param ExptMethods [out]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/bf564898-e540-458b-861c-0f57082d40a1">RTM_ENTITY_EXPORT_METHOD</a> structure that contains the set of method identifiers requested by the calling client.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer supplied is not large enough to hold all the requested information.

</td>
</tr>
</table>
 




## -remarks



Do not call another client's method directly, always use 
<a href="https://msdn.microsoft.com/97506565-2fa7-4ff7-b397-7ab712759a5d">RtmInvokeMethod</a>. The routing table manager performs error checking when using 
<b>RtmInvokeMethod</b> to ensure that the client is not unregistering or already unregistered.

If ERROR_INSUFFICIENT_BUFFER is returned, there may be some data in <i>ExptMethods</i>; <i>NumMethods</i> specifies how many methods actually fit in the buffer.

When the entity handle is no longer required, release it by calling 
<a href="https://msdn.microsoft.com/1f6c4275-0129-4f27-b9b2-bfda33d34d21">RtmReleaseEntities</a>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/55b2a03f-498c-4321-891b-747f4baea10d">Obtain and Call the Exported Methods for a Client</a>.




## -see-also




<a href="https://msdn.microsoft.com/492bb2bf-5b35-4eef-a039-3d3e1137220f">RtmBlockMethods</a>



<a href="https://msdn.microsoft.com/97506565-2fa7-4ff7-b397-7ab712759a5d">RtmInvokeMethod</a>
 

 

