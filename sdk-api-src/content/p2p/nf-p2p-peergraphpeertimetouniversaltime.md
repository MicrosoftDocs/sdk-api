---
UID: NF:p2p.PeerGraphPeerTimeToUniversalTime
title: PeerGraphPeerTimeToUniversalTime function (p2p.h)
description: The PeerGraphPeerTimeToUniversalTime function converts the peer graph-maintained reference time value to a localized time value appropriate for display on the peer's computer.
helpviewer_keywords: ["PeerGraphPeerTimeToUniversalTime","PeerGraphPeerTimeToUniversalTime function [Peer Networking]","p2p.peergraphpeertimetouniversaltime","p2p/PeerGraphPeerTimeToUniversalTime"]
old-location: p2p\peergraphpeertimetouniversaltime.htm
tech.root: p2p
ms.assetid: 9cbb0b59-c116-4bd2-932f-2140595f4fad
ms.date: 12/05/2018
ms.keywords: PeerGraphPeerTimeToUniversalTime, PeerGraphPeerTimeToUniversalTime function [Peer Networking], p2p.peergraphpeertimetouniversaltime, p2p/PeerGraphPeerTimeToUniversalTime
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
 - PeerGraphPeerTimeToUniversalTime
 - p2p/PeerGraphPeerTimeToUniversalTime
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
 - PeerGraphPeerTimeToUniversalTime
---

# PeerGraphPeerTimeToUniversalTime function


## -description

The <b>PeerGraphPeerTimeToUniversalTime</b> function converts the peer graph-maintained reference time value to a localized time value appropriate for display on the peer's computer.

## -parameters

### -param hGraph [in]

Handle to the  peer graph this peer participates in. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a> function.

### -param pftPeerTime [in]

Pointer to the peer time (UTC)  value, represented as a <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure.

### -param pftUniversalTime [out]

Pointer to the returned universal time value, represented as a <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure.

## -returns

Returns S_OK if the function succeeds; otherwise, the function returns one of the following values.

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
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

<i>Universal time</i> is the UTC time derived from the peer's system clock.

<i>Peer time</i> is a common reference time maintained by the peer graph, expressed as Greenwich Mean Time.

Peer time should be  converted to universal time whenever it is necessary to display this value on the peer's computer, such as when displaying the creation time of a record. Likewise, time-sensitive actions, such as setting the expiration time for a record or searching for records based on modification time, should use time values converted from the computer-specific universal time to graph-specific peer time.

Universal time can be converted to peer time by calling the converse function <a href="/windows/desktop/api/p2p/nf-p2p-peergraphuniversaltimetopeertime">PeerGraphUniversalTimeToPeerTime</a>.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphuniversaltimetopeertime">PeerGraphUniversalTimeToPeerTime</a>