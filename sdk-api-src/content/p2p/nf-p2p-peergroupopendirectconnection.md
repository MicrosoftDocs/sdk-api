---
UID: NF:p2p.PeerGroupOpenDirectConnection
title: PeerGroupOpenDirectConnection function (p2p.h)
description: The PeerGroupOpenDirectConnection function establishes a direct connection with another peer in a peer group.
helpviewer_keywords: ["PeerGroupOpenDirectConnection","PeerGroupOpenDirectConnection function [Peer Networking]","p2p.peergroupopendirectconnection","p2p/PeerGroupOpenDirectConnection"]
old-location: p2p\peergroupopendirectconnection.htm
tech.root: p2p
ms.assetid: a3c52754-91b0-4722-a459-87c70b3ab9ad
ms.date: 12/05/2018
ms.keywords: PeerGroupOpenDirectConnection, PeerGroupOpenDirectConnection function [Peer Networking], p2p.peergroupopendirectconnection, p2p/PeerGroupOpenDirectConnection
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
 - PeerGroupOpenDirectConnection
 - p2p/PeerGroupOpenDirectConnection
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
 - PeerGroupOpenDirectConnection
---

# PeerGroupOpenDirectConnection function


## -description

The <b>PeerGroupOpenDirectConnection</b> function establishes a direct connection with another peer in a peer group.

## -parameters

### -param hGroup [in]

Handle to the peer group that hosts the direct connection. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pwzIdentity [in]

Pointer to a Unicode string that contains the identity   a peer  connects to. This parameter is required.

### -param pAddress [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structure that contains the IPv6 address   the peer  connects to. This parameter is required.

### -param pullConnectionId [out]

Unsigned 64-bit integer that identifies the direct connection. This ID value cannot be assumed as valid until the <a href="/windows/desktop/api/p2p/ne-p2p-peer_group_event_type">PEER_GROUP_EVENT_DIRECT_CONNECTION</a> event is raised and indicates that the connection has been accepted by the other peer. This parameter is required.

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
<dt><b>PEER_E_CONNECT_SELF</b></dt>
</dl>
</td>
<td width="60%">
The connection failed because it was a loopback, that is, the connection is between a peer and itself.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. This is typically caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

Every direct connection opened with this function must be closed with [PEER_GROUP_EVENT DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure has the  <b>status</b> member of its component <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_connection_change_data">PEER_EVENT_CONNECTION_CHANGE_DATA</a> structure set to PEER_CONNECTION_FAILED.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address"> PEER_ADDRESS</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_connection_change_data">PEER_EVENT_CONNECTION_CHANGE_DATA</a>



[PEER_GROUP_EVENT DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/ne-p2p-peer_group_event_type">PEER_GROUP_EVENT_DIRECT_CONNECTION</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupclosedirectconnection">PeerGroupCloseDirectConnection</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupsenddata">PeerGroupSendData</a>