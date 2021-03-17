---
UID: NF:p2p.PeerGroupRegisterEvent
title: PeerGroupRegisterEvent function (p2p.h)
description: The PeerGroupRegisterEvent function registers a peer for specific peer group events.
helpviewer_keywords: ["PeerGroupRegisterEvent","PeerGroupRegisterEvent function [Peer Networking]","p2p.peergroupregisterevent","p2p/PeerGroupRegisterEvent"]
old-location: p2p\peergroupregisterevent.htm
tech.root: p2p
ms.assetid: a4dc100a-d3dc-408e-a425-bded11d04db5
ms.date: 12/05/2018
ms.keywords: PeerGroupRegisterEvent, PeerGroupRegisterEvent function [Peer Networking], p2p.peergroupregisterevent, p2p/PeerGroupRegisterEvent
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
 - PeerGroupRegisterEvent
 - p2p/PeerGroupRegisterEvent
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
 - PeerGroupRegisterEvent
---

# PeerGroupRegisterEvent function


## -description

The <b>PeerGroupRegisterEvent</b> function registers a peer for specific peer group events.

## -parameters

### -param hGroup [in]

Handle of the peer group on which to monitor the specific peer events. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param hEvent [in]

Pointer to a Windows  event handle, which is signaled when a peer event is fired. When this handle is signaled, the peer should call <a href="/windows/desktop/api/p2p/nf-p2p-peergroupgeteventdata">PeerGroupGetEventData</a> until the function returns <b>PEER_S_NO_EVENT_DATA</b>.  This parameter is required.

### -param cEventRegistration [in]

Contains the number of <a href="/windows/desktop/api/p2p/ns-p2p-peer_group_event_registration">PEER_GROUP_EVENT_REGISTRATION</a> structures listed in <i>pEventRegistrations</i>. This parameter is required.

### -param pEventRegistrations [in]

Pointer to a list of <a href="/windows/desktop/api/p2p/ns-p2p-peer_group_event_registration">PEER_GROUP_EVENT_REGISTRATION</a> 
		 structures that contains the peer event types for which registration  occurs. This parameter is required.

### -param phPeerEvent [out]

Pointer to the returned HPEEREVENT handle. A peer can unregister for this peer event by passing this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupunregisterevent">PeerGroupUnregisterEvent</a>. This parameter is required.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

Before you close the HPEEREVENT handle, you must unregister for the peer event  types by passing the handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupunregisterevent">PeerGroupUnregisterEvent</a>.

## -see-also

[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/ns-p2p-peer_group_event_registration">PEER_GROUP_EVENT_REGISTRATION</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupgeteventdata">PeerGroupGetEventData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupunregisterevent">PeerGroupUnregisterEvent</a>