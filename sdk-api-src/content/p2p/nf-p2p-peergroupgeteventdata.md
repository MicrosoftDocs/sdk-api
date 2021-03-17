---
UID: NF:p2p.PeerGroupGetEventData
title: PeerGroupGetEventData function (p2p.h)
description: The PeerGroupGetEventData function allows an application to retrieve the data returned by a grouping event.
helpviewer_keywords: ["PeerGroupGetEventData","PeerGroupGetEventData function [Peer Networking]","p2p.peergroupgeteventdata","p2p/PeerGroupGetEventData"]
old-location: p2p\peergroupgeteventdata.htm
tech.root: p2p
ms.assetid: bc742c09-190d-412e-ae1a-f1350b3748f5
ms.date: 12/05/2018
ms.keywords: PeerGroupGetEventData, PeerGroupGetEventData function [Peer Networking], p2p.peergroupgeteventdata, p2p/PeerGroupGetEventData
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGroupGetEventData
 - p2p/PeerGroupGetEventData
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
 - PeerGroupGetEventData
---

# PeerGroupGetEventData function


## -description

The <b>PeerGroupGetEventData</b> function allows an application to retrieve the data returned by a grouping event.

## -parameters

### -param hPeerEvent [in]

Handle obtained from a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupregisterevent">PeerGroupRegisterEvent</a>. This parameter is required.

### -param ppEventData [out]

Pointer to a [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure that contains data about the peer event. This data structure must be freed after use with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>. This parameter is required.

## -returns

Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns one of the following values.

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
<dt><b>PEER_S_NO_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The call is successful, but there is no event data available.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

When an event occurs for which a peer has requested notification, the corresponding peer event handle is signaled. The peer  calls this method until [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structures are retrieved. Each data structure contains the following two key pieces of data: 

<ul>
<li>The registration associated with a peer event.</li>
<li>The actual data for a peer event.</li>
</ul>

## -see-also

[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupregisterevent">PeerGroupRegisterEvent</a>