---
UID: NF:p2p.PeerCollabGetEventData
title: PeerCollabGetEventData function (p2p.h)
description: Obtains the data associated with a peer collaboration event raised on the peer.
helpviewer_keywords: ["PeerCollabGetEventData","PeerCollabGetEventData function [Peer Networking]","p2p.peercollabgeteventdata","p2p/PeerCollabGetEventData"]
old-location: p2p\peercollabgeteventdata.htm
tech.root: p2p
ms.assetid: ee410a47-91a6-48ed-8c05-128a141a5c98
ms.date: 12/05/2018
ms.keywords: PeerCollabGetEventData, PeerCollabGetEventData function [Peer Networking], p2p.peercollabgeteventdata, p2p/PeerCollabGetEventData
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
 - PeerCollabGetEventData
 - p2p/PeerCollabGetEventData
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
 - PeerCollabGetEventData
---

# PeerCollabGetEventData function


## -description

The <b>PeerCollabGetEventData</b> function obtains the data associated with a peer collaboration event raised on the peer.

## -parameters

### -param hPeerEvent [in]

The peer collaboration network event handle obtained by a call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterevent">PeerCollabRegisterEvent</a>.

### -param ppEventData [out]

Pointer to a list of [PEER_COLLAB_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_collab_event_data-r1) structures that contain data about the peer collaboration network event. These data structures must be freed after use by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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
<dt><b>PEER_S_NO_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The  event data is not present.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>