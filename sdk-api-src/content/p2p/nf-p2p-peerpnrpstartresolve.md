---
UID: NF:p2p.PeerPnrpStartResolve
title: PeerPnrpStartResolve function (p2p.h)
description: Starts an asynchronous peer name resolution operation.
helpviewer_keywords: ["PeerPnrpStartResolve","PeerPnrpStartResolve function [Peer Networking]","p2p.peerpnrpstartresolve","p2p/PeerPnrpStartResolve"]
old-location: p2p\peerpnrpstartresolve.htm
tech.root: p2p
ms.assetid: 140ecca5-85fe-480e-bc69-86e0bc69ad2e
ms.date: 12/05/2018
ms.keywords: PeerPnrpStartResolve, PeerPnrpStartResolve function [Peer Networking], p2p.peerpnrpstartresolve, p2p/PeerPnrpStartResolve
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PeerPnrpStartResolve
 - p2p/PeerPnrpStartResolve
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
 - PeerPnrpStartResolve
---

# PeerPnrpStartResolve function


## -description

The <b>PeerPnrpStartResolve</b> function starts an asynchronous peer name resolution operation.

## -parameters

### -param pcwzPeerName [in]

Pointer to a zero-terminated string that contains the peer name for which endpoint addresses will be obtained.

### -param pcwzCloudName [in, optional]

Pointer to a zero-terminated string that contains the name of the PNRP cloud under which to resolve the peer name. If <b>NULL</b>, resolution is performed for all clouds. If PEER_PNRP_ALL_LINK_CLOUDS, resolution is performed for all link local clouds. When "GLOBAL_" is specified, resolution takes place in the global cloud.

### -param cMaxEndpoints [in, optional]

The maximum number of endpoints to return for the peer name.

### -param hEvent [in]

Handle to the event signaled when a peer endpoint is resolved for the supplied peer name and are ready for consumption by calling PeerPnrpGetEndpoint. This event is signaled for every endpoint discovered by the PNRP service. If PEER_NO_MORE is returned by a call to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpgetendpoint">PeerPnrpGetEndpoint</a>, then all endpoints have been found for that peer.

### -param phResolve [out]

Handle to this peer name resolution request. This handle must be provided to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpendresolve">PeerPnrpEndResolve</a> after the resolution events are raised and the endpoints are obtained with corresponding calls to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpgetendpoint">PeerPnrpGetEndpoint</a>, or if the operation fails.

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
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>

## -remarks

<b>PeerPnrpStartResolve</b> creates a handle to an asynchronous peer name resolution operation. 

Whenever an endpoint is found, the event handle provided in <i>hEvent</i> is signaled, and <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpgetendpoint">PeerPnrpGetEndpoint</a> must be called with the <i>phResolve</i> handle by the application to obtain that endpoint.

The last event specifies the PEER_E_NO_MORE error code, indicating that all endpoints corresponding to the peer name supplied to <b>PeerPnrpStartResolve</b> have been found. At this time, the application must close the handle with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpendresolve">PeerPnrpEndResolve</a>.

A handle must be resolved in a process separate from the process in which it was registered. If a handle is registered and resolved within the same process it will not be recognized.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpendresolve">PeerPnrpEndResolve</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpgetendpoint">PeerPnrpGetEndpoint</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpresolve">PeerPnrpResolve</a>