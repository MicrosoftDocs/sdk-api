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

# PeerCollabGetApplicationRegistrationInfo function


## -description


The <b>PeerCollabGetApplicationRegistrationInfo</b> function obtains application-specific registration information.


## -parameters




### -param pApplicationId [in]

Pointer to the GUID value that represents a particular peer's application registration flags.


### -param registrationType [in]

A <a href="https://msdn.microsoft.com/58f14e46-377e-494b-93ef-fc19e8d87fcc">PEER_APPLICATION_REGISTRATION_TYPE</a> enumeration value that describes whether the peer's application is registered to the current user or all users of the local machine.


### -param ppApplication

TBD




#### - ppRegInfo [out]

Pointer to the address of a <a href="https://msdn.microsoft.com/64c9eb02-3235-4824-8de1-352b0a1ffbb4">PEER_APPLICATION_REGISTRATION_INFO</a> structure that contains the information about a peer's specific registered application. The data returned in this parameter can be freed by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>. 


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested application is not registered for the given <i>registrationType</i>.

</td>
</tr>
</table>
 




## -remarks



An <i>application</i> is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer's application has a GUID representing a single application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To unregister a peer's application, call <a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a> with this GUID.




## -see-also




<a href="https://msdn.microsoft.com/64c9eb02-3235-4824-8de1-352b0a1ffbb4">PEER_APPLICATION_REGISTRATION_INFO</a>



<a href="https://msdn.microsoft.com/58f14e46-377e-494b-93ef-fc19e8d87fcc">PEER_APPLICATION_REGISTRATION_TYPE</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/962982a6-171f-4c13-ae03-84698482dea4">PeerCollabRegisterApplication</a>



<a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a>
 

 

