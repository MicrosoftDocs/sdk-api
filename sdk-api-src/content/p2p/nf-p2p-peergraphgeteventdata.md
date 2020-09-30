---
UID: NF:p2p.PeerGraphGetEventData
title: PeerGraphGetEventData function (p2p.h)
description: The PeerGraphGetEventData function retrieves peer events. An application calls this function until the return value PEER_S_NO_EVENT_DATA is returned, which indicates that a call is successful, but that there are no more peer events to retrieve.
helpviewer_keywords: ["PeerGraphGetEventData","PeerGraphGetEventData function [Peer Networking]","p2p.peergraphgeteventdata","p2p/PeerGraphGetEventData"]
old-location: p2p\peergraphgeteventdata.htm
tech.root: p2p
ms.assetid: b64bb920-3fbc-4927-a1b1-39c99850bdd5
ms.date: 12/05/2018
ms.keywords: PeerGraphGetEventData, PeerGraphGetEventData function [Peer Networking], p2p.peergraphgeteventdata, p2p/PeerGraphGetEventData
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGraphGetEventData
 - p2p/PeerGraphGetEventData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphGetEventData
---

# PeerGraphGetEventData function


## -description

The <b>PeerGraphGetEventData</b> function retrieves peer events. An application  calls this function until the  return value   <b>PEER_S_NO_EVENT_DATA</b> is returned, which indicates that a call is successful, but that there are no more peer events to retrieve.

## -parameters

### -param hPeerEvent [in]

Peer event handle obtained by a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerGraphRegisterEvent</a>.

### -param ppEventData [out]

Receives a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a> structure that contains the data about an event notification.   When this structure is not needed, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>.

## -returns

If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

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
One parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_S_NO_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The function call succeeds, but there is no data associated with a peer event.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

Peer event data is returned in  a <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a> structure.  The type of data structure that <b>PEER_GRAPH_EVENT_DATA</b> points to depends  on which event is triggered.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerGraphRegisterEvent</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphunregisterevent">PeerGraphUnregisterEvent</a>