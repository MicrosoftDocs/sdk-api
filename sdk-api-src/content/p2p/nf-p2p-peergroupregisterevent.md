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

# PeerGroupRegisterEvent function


## -description



      The <b>PeerGroupRegisterEvent</b> function registers a peer for specific peer group events.


## -parameters




### -param hGroup [in]

Handle of the peer group on which to monitor the specific peer events. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param hEvent [in]

Pointer to a Windows  event handle, which is signaled when a peer event is fired. When this handle is signaled, the peer should call <a href="https://msdn.microsoft.com/bc742c09-190d-412e-ae1a-f1350b3748f5">PeerGroupGetEventData</a> until the function returns <b>PEER_S_NO_EVENT_DATA</b>.  This parameter is required.


### -param cEventRegistration [in]

Contains the number of <a href="https://msdn.microsoft.com/9c9c82c3-b02a-49c2-9a8f-eb355ded8480">PEER_GROUP_EVENT_REGISTRATION</a> structures listed in <i>pEventRegistrations</i>. This parameter is required.


### -param pEventRegistrations [in]

Pointer to a list of <a href="https://msdn.microsoft.com/9c9c82c3-b02a-49c2-9a8f-eb355ded8480">PEER_GROUP_EVENT_REGISTRATION</a> 
		 structures that contains the peer event types for which registration  occurs. This parameter is required.


### -param phPeerEvent [out]

Pointer to the returned HPEEREVENT handle. A peer can unregister for this peer event by passing this handle to <a href="https://msdn.microsoft.com/ad13cbf6-0dc9-4de5-aae7-2ecf6af90ea6">PeerGroupUnregisterEvent</a>. This parameter is required.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



Before you close the HPEEREVENT handle, you must unregister for the peer event  types by passing the handle to <a href="https://msdn.microsoft.com/ad13cbf6-0dc9-4de5-aae7-2ecf6af90ea6">PeerGroupUnregisterEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/9c9c82c3-b02a-49c2-9a8f-eb355ded8480">
		  PEER_GROUP_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/bc742c09-190d-412e-ae1a-f1350b3748f5">PeerGroupGetEventData</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/ad13cbf6-0dc9-4de5-aae7-2ecf6af90ea6">PeerGroupUnregisterEvent</a>
 

 

