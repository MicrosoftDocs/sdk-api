---
UID: NF:p2p.PeerCollabEnumApplicationRegistrationInfo
title: PeerCollabEnumApplicationRegistrationInfo function
author: windows-sdk-content
description: Obtains the enumeration handle used to retrieve peer application information.
old-location: p2p\peercollabenumapplicationregistrationinfo.htm
tech.root: P2PSdk
ms.assetid: 635af767-a4b5-4c48-9966-35c1a629db5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerCollabEnumApplicationRegistrationInfo, PeerCollabEnumApplicationRegistrationInfo function [Peer Networking], p2p.peercollabenumapplicationregistrationinfo, p2p/PeerCollabEnumApplicationRegistrationInfo
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabEnumApplicationRegistrationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerCollabEnumApplicationRegistrationInfo function


## -description


The <b>PeerCollabEnumApplicationRegistrationInfo</b> function obtains the enumeration handle used to retrieve peer application  information.


## -parameters




### -param registrationType [in]

A <a href="https://msdn.microsoft.com/58f14e46-377e-494b-93ef-fc19e8d87fcc">PEER_APPLICATION_REGISTRATION_TYPE</a> value that specifies whether the peer's application is registered to the <b>current user</b> or <b>all users</b> of the peer's machine.


### -param phPeerEnum [out]

Pointer to a peer enumeration handle for the peer application registration information. This data is obtained by passing this handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>.


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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

</td>
</tr>
</table>
 




## -remarks



To obtain the individual peer applications, pass the returned handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>. An array of <a href="https://msdn.microsoft.com/64c9eb02-3235-4824-8de1-352b0a1ffbb4">PEER_APPLICATION_REGISTRATION_INFO</a> structures will be returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.

An <i>application</i> is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer's application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To unregister a peer's application, call <a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a> with this GUID.

Peer application registration information items are returned as individual <a href="https://msdn.microsoft.com/64c9eb02-3235-4824-8de1-352b0a1ffbb4">PEER_APPLICATION_REGISTRATION_INFO</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/64c9eb02-3235-4824-8de1-352b0a1ffbb4">PEER_APPLICATION_REGISTRATION_INFO</a>



<a href="https://msdn.microsoft.com/58f14e46-377e-494b-93ef-fc19e8d87fcc">PEER_APPLICATION_REGISTRATION_TYPE</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a>
 

 

