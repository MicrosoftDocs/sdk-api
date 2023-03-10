---
UID: NF:p2p.PeerPnrpResolve
title: PeerPnrpResolve function (p2p.h)
description: Obtains the endpoint address(es) registered for a specific peer name.
helpviewer_keywords: ["PeerPnrpResolve","PeerPnrpResolve function [Peer Networking]","p2p.peerpnrpresolve","p2p/PeerPnrpResolve"]
old-location: p2p\peerpnrpresolve.htm
tech.root: p2p
ms.assetid: dd66ab38-bb3e-46f5-943a-bcdae90acae0
ms.date: 12/05/2018
ms.keywords: PeerPnrpResolve, PeerPnrpResolve function [Peer Networking], p2p.peerpnrpresolve, p2p/PeerPnrpResolve
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
 - PeerPnrpResolve
 - p2p/PeerPnrpResolve
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
 - PeerPnrpResolve
---

# PeerPnrpResolve function


## -description

The <b>PeerPnrpResolve</b> function obtains the endpoint address(es) registered for a specific peer name.

## -parameters

### -param pcwzPeerName [in]

Pointer to a zero-terminated string that contains the peer name for which endpoint addresses will be obtained.

### -param pcwzCloudName [in, optional]

Pointer to a zero-terminated string that contains the name of the PNRP cloud under which to resolve the peer name. If <b>NULL</b>, the resolve is performed in all clouds. If PEER_PNRP_ALL_LINK_CLOUDS, the resolve is performed in all link local clouds. When "GLOBAL_", resolve will only take place in the global cloud.

### -param pcEndpoints [in, out]

The maximum number of endpoints to return in  <i>ppEndpoints</i>. Upon return, this parameter contains the actual number of endpoints in <i>ppEndpoints</i>.

### -param ppEndpoints [out]

Pointer to a list of <a href="/windows/desktop/api/p2p/ns-p2p-peer_pnrp_endpoint_info">PEER_PNRP_ENDPOINT_INFO</a> structures that contain the endpoints for which the peer name successfully resolved. Each endpoint contains one or more IP addresses at which the peer node can be reached.

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

This call is synchronous and will block until completed. For asynchronous peer name resolution, call <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartresolve">PeerPnrpStartResolve</a> and obtain the resolved endpoint address when the supplied event is raised.

A handle must be resolved in a process separate of the process it was registered in. If a handle is registered and resolved within the same process it will not be recognized.

When  resolution is performed for all clouds, it is issued to each cloud simultaneously. The method will return as soon as it has received enough results from any combination of clouds.

The default resolve timeout used internally by this method is 30 seconds. If a  specific timeout is required,the asynchronous <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartresolve">PeerPnrpStartResolve</a> function should be used.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartresolve">PeerPnrpStartResolve</a>