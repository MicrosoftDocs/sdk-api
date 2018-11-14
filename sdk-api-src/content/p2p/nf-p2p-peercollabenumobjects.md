---
UID: NF:p2p.PeerCollabEnumObjects
title: PeerCollabEnumObjects function
author: windows-sdk-content
description: Returns the handle to an enumeration that contains the peer objects associated with a specific peer's endpoint.
old-location: p2p\peercollabenumobjects.htm
tech.root: P2PSdk
ms.assetid: a9ac2603-b007-4d1c-ac11-c72aeb06e663
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerCollabEnumObjects, PeerCollabEnumObjects function [Peer Networking], p2p.peercollabenumobjects, p2p/PeerCollabEnumObjects
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PeerCollabEnumObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PeerCollabEnumObjects
: 
---

# PeerCollabEnumObjects function


## -description


The <b>PeerCollabEnumObjects</b> function returns the handle to an enumeration that contains the peer objects associated with a specific peer's endpoint.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the endpoint information for a peer whose objects will be enumerated. 

If this parameter is <b>NULL</b> the published objects of the  local peer's contacts are returned.


### -param pObjectId [in, optional]

Pointer to a GUID value that uniquely identifies a peer object with the supplied peer. If this parameter is supplied, the only peer object returned is the one that matches this GUID.


### -param phPeerEnum [out]

Pointer to the handle for the enumerated set of peer objects that correspond to the GUID returned in <i>pObjectId</i>. Pass this handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> to obtain each item in the enumerated set.


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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The operation requires the user to be signed in.

</td>
</tr>
</table>
 




## -remarks



Peer objects are run-time data items associated with a particular application, such as a picture, an avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size.

<b>PeerCollabEnumObjects</b> will return all of the objects published for the local peer. The objects can be published by more than one application.

To obtain the individual peer objects, pass the returned handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>. The peer objects are returned as an array of pointers to the <a href="https://msdn.microsoft.com/6babceaf-9648-4226-a0ce-6f4ae831e4a7">PEER_OBJECT</a> structures. If the endpoint is not publishing any objects, an empty array will be returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.

To obtain a peer object successfully:<ul>
<li>The endpoint must have been previously obtained by calling <a href="https://msdn.microsoft.com/c29d089c-1f1e-4d50-9a3a-18c844b4ad1c">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>


If the user is publishing a picture, the picture can be obtained by retrieving the corresponding object. The GUID for the picture object is PEER_COLLAB_OBJECTID_USER_PICTURE.




## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/6babceaf-9648-4226-a0ce-6f4ae831e4a7">PEER_OBJECT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

