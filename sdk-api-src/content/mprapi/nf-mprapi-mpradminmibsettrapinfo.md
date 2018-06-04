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

# MprAdminMIBSetTrapInfo function


## -description


The 
<b>MprAdminMIBSetTrapInfo</b> function specifies a handle to an event that is signaled whenever a TRAP needs to be issued.


## -parameters




### -param dwProtocolId

TBD


### -param dwRoutingPid [in]

Specifies a <b>DWORD</b> variable that contains the identifier of the routing protocol.


### -param hEvent [in]

Handle to an event that is signaled when a trap needs to be issued.


### -param lpInData [in]

Pointer to the input data.


### -param dwInDataSize [in]

Specifies a <b>DWORD</b> variable that contains the size in bytes of the data pointed to by <i>lpInData</i>.


### -param lplpOutData [out]

Receives the address of a pointer to the output data.


### -param lpOutDataSize

TBD




#### - dwTransportId [in]

Specifies a <b>DWORD</b> variable that contains the protocol family identifier.


#### - lpdwOutDataSize [in, out]

On input, pointer to a <b>DWORD</b> variable. 




On output, receives the size, in bytes, of the data pointed to by <i>* lplpOutData</i>.


## -returns



If the functions succeeds, the return value is NO_ERROR

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any installed router manager.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/626c66c8-db7b-4be3-b5b0-c10a41ca46cc">MprAdminMIBGetTrapInfo</a>



<a href="https://msdn.microsoft.com/c911daa4-4f3d-4944-9dc0-695a4efbcb1b">Router Management MIB Functions</a>



<a href="https://msdn.microsoft.com/a7a28ac0-c6f9-450c-9925-67990a62ba08">Router Management MIB Reference</a>



<a href="https://msdn.microsoft.com/3d9e21de-1eca-4e3f-a941-5f7b0f46e30c">Transport and Protocol Constants</a>
 

 

