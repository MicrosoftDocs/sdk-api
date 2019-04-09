---
UID: NF:p2p.PeerCollabEnumApplications
title: PeerCollabEnumApplications function (p2p.h)
author: windows-sdk-content
description: Returns the handle to an enumeration that contains the applications registered to a specific peer's endpoint(s).
old-location: p2p\peercollabenumapplications.htm
tech.root: P2PSdk
ms.assetid: 550cbd9d-5569-485e-897d-73d8bab8430a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerCollabEnumApplications, PeerCollabEnumApplications function [Peer Networking], p2p.peercollabenumapplications, p2p/PeerCollabEnumApplications
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
 - PeerCollabEnumApplications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerCollabEnumApplications function


## -description


The <b>PeerCollabEnumApplications</b> function returns the handle to an enumeration that contains the applications registered to a specific peer's endpoint(s).


## -parameters




### -param pcEndpoint [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the endpoint information for a peer whose applications will be enumerated. 

If this parameter is set to <b>NULL</b>, the published application information for the local peer's endpoint is enumerated.


### -param pApplicationId [in, optional]

Pointer to the GUID value that uniquely identifies a particular application of the supplied peer. If this parameter is supplied, the only peer application returned is the one that matches this GUID.


### -param phPeerEnum [out]

Pointer to the handle for the enumerated set of registered applications that correspond to the GUID returned in <i>pObjectId</i>. Pass this handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> to obtain each item in the enumerated set.


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



In order to enumerate the applications for the specified endpoint  successfully, application data must be available on the endpoint. For application data to be available, one of the following must occur:<ul>
<li>The endpoint must have been previously obtained by calling <a href="https://msdn.microsoft.com/c29d089c-1f1e-4d50-9a3a-18c844b4ad1c">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>


To obtain the individual peer applications, pass the returned handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>. To close the enumeration and release the resources associated with it, pass this handle to <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.

Peer application data items are returned as individual <a href="https://msdn.microsoft.com/a219231b-75d0-47d3-8294-f1cc25b43d27">PEER_APPLICATION</a> structures.

The <b>PeerCollabEnumApplications</b> function returns an empty array for endpoints on the subnet that are not trusted contacts.




## -see-also




<a href="https://msdn.microsoft.com/a219231b-75d0-47d3-8294-f1cc25b43d27">PEER_APPLICATION</a>



<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

