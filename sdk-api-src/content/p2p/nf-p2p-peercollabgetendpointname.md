---
UID: NF:p2p.PeerCollabGetEndpointName
title: PeerCollabGetEndpointName function (p2p.h)
description: Retrieves the name of the current endpoint of the calling peer, as previously set by a call to PeerCollabSetEndpointName.
old-location: p2p\peercollabgetendpointname.htm
tech.root: P2PSdk
ms.assetid: f6165772-be55-4b56-bc70-dfa2c4a40c61
ms.date: 12/05/2018
ms.keywords: PeerCollabGetEndpointName, PeerCollabGetEndpointName function [Peer Networking], p2p.peercollabgetendpointname, p2p/PeerCollabGetEndpointName
f1_keywords:
- p2p/PeerCollabGetEndpointName
dev_langs:
- c++
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
- PeerCollabGetEndpointName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerCollabGetEndpointName function


## -description


The <b>PeerCollabGetEndpointName</b> function retrieves the name of the current endpoint of the calling peer, as previously set by a call to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peercollabsetendpointname">PeerCollabSetEndpointName</a>.


## -parameters




### -param ppwzEndpointName [out]

Pointer to a zero-terminated Unicode string name of the peer endpoint currently used by the calling application.


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



The endpoint name is limited to 25 Unicode characters. To free this data call <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peercollabsetendpointname">PeerCollabSetEndpointName</a>
 

 

