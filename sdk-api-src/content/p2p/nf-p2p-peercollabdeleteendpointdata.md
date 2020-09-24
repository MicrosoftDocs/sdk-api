---
UID: NF:p2p.PeerCollabDeleteEndpointData
title: PeerCollabDeleteEndpointData function (p2p.h)
description: Deletes the peer endpoint data on the calling peer node that matches the supplied endpoint data.
helpviewer_keywords: ["PeerCollabDeleteEndpointData","PeerCollabDeleteEndpointData function [Peer Networking]","p2p.peercollabdeleteendpointdata","p2p/PeerCollabDeleteEndpointData"]
old-location: p2p\peercollabdeleteendpointdata.htm
tech.root: p2p
ms.assetid: bafaef04-d7f6-4873-bd38-db156817b0c8
ms.date: 12/05/2018
ms.keywords: PeerCollabDeleteEndpointData, PeerCollabDeleteEndpointData function [Peer Networking], p2p.peercollabdeleteendpointdata, p2p/PeerCollabDeleteEndpointData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerCollabDeleteEndpointData
 - p2p/PeerCollabDeleteEndpointData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabDeleteEndpointData
---

# PeerCollabDeleteEndpointData function


## -description

The <b>PeerCollabDeleteEndpointData</b> function deletes the peer endpoint data on the calling peer node that matches the supplied endpoint data.

## -parameters

### -param pcEndpoint [in]

Pointer to a [PEER_ENDPOINT](./ns-p2p-peer_endpoint.md) structure that contains the peer endpoint information to delete from the current peer node.

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
</table>

## -remarks

The function <b>PeerCollabDeleteEndpointData</b> is used to remove cached endpoint data previously retrieved by  <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> when it is no longer required. Any data obtained through <b>PeerCollabRefreshEndpointData</b> remains in memory until <b>PeerCollabDeleteEndpointData</b> is called.

## -see-also

[PEER_ENDPOINT](./ns-p2p-peer_endpoint.md)



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a>