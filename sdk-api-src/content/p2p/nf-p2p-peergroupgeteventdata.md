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

# PeerGroupGetEventData function


## -description



      The <b>PeerGroupGetEventData</b> function allows an application to retrieve the data returned by a grouping event.


## -parameters




### -param hPeerEvent [in]

Handle obtained from a previous call to <a href="https://msdn.microsoft.com/a4dc100a-d3dc-408e-a425-bded11d04db5">PeerGroupRegisterEvent</a>. This parameter is required.


### -param ppEventData [out]

Pointer to a <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a> structure that contains data about the peer event. This data structure must be freed after use with <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>. This parameter is required.


## -returns



Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_S_NO_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The call is successful, but there is no event data available.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks




        When an event occurs for which a peer has requested notification, the corresponding peer event handle is signaled. The peer  calls this method until <b>PEER_S_NO_EVENT_DATA</b> is returned, when all of the associated <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a> structures are retrieved. Each data structure contains the following two key pieces of data: 

<ul>
<li>The registration associated with a peer event.</li>
<li>The actual data for a peer event.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">
		  PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>



<a href="https://msdn.microsoft.com/a4dc100a-d3dc-408e-a425-bded11d04db5">PeerGroupRegisterEvent</a>
 

 

