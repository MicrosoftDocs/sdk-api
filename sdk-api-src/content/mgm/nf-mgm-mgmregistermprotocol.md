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

# MgmRegisterMProtocol function


## -description


The 
<b>MgmRegisterMProtocol</b> function is used by clients to register with the multicast group manager. When the registration is complete, the multicast group manager returns a handle to the client. The client must supply this handle in subsequent MGM function calls.


## -parameters




### -param prpiInfo [in]

Pointer to a 
<a href="https://msdn.microsoft.com/acbf0519-a0c8-4b96-9722-9eeccee026d7">ROUTING_PROTOCOL_CONFIG</a> structure that contains pointers to callbacks into the client.


### -param dwProtocolId [in]

Specifies the ID of the client. The ID is unique for each client.


### -param dwComponentId [in]

Specifies the component ID for a specific instance of the client. This parameter is used with <i>dwProtocolId</i> to uniquely identify an instance of a client.


### -param phProtocol [out]

On input, the client must supply a pointer to a handle. 




On output, <i>phProtocol</i> receives the registration handle for the client. This handle must be used in subsequent calls to the multicast group manager.


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
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Cannot register the specified client because an entry with the same protocol ID and component ID already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



Registering a protocol is the first operation any multicast routing protocol should perform. After registration, a routing protocol should take ownership of the appropriate interfaces before adding or deleting group memberships.

Only one routing protocol may take ownership of an interface at any given time. Multiple routing protocols may be registered with the multicast group manager, each protocol owning different interfaces.




## -see-also




<a href="https://msdn.microsoft.com/e9b2613e-4e52-4993-81dd-0be50a072db6">MgmDeRegisterMProtocol</a>



<a href="https://msdn.microsoft.com/b072c884-0b84-4dd9-a14c-185f5d327017">MgmTakeInterfaceOwnership</a>



<a href="https://msdn.microsoft.com/acbf0519-a0c8-4b96-9722-9eeccee026d7">ROUTING_PROTOCOL_CONFIG</a>
 

 

