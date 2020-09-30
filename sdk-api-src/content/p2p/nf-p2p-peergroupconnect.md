---
UID: NF:p2p.PeerGroupConnect
title: PeerGroupConnect function (p2p.h)
description: The PeerGroupConnect function initiates a PNRP search for a peer group and attempts to connect to it. After this function is called successfully, a peer can communicate with other members of the peer group.
helpviewer_keywords: ["PeerGroupConnect","PeerGroupConnect function [Peer Networking]","p2p.peergroupconnect","p2p/PeerGroupConnect"]
old-location: p2p\peergroupconnect.htm
tech.root: p2p
ms.assetid: 240bcba7-29f9-4043-8203-e71175bee69a
ms.date: 12/05/2018
ms.keywords: PeerGroupConnect, PeerGroupConnect function [Peer Networking], p2p.peergroupconnect, p2p/PeerGroupConnect
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
 - PeerGroupConnect
 - p2p/PeerGroupConnect
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
 - PeerGroupConnect
---

# PeerGroupConnect function


## -description

The <b>PeerGroupConnect</b> function initiates a PNRP search for a peer group and attempts to connect to it. After this function is  called successfully, a peer can communicate with other members of the peer group.

## -parameters

### -param hGroup [in]

Handle to the peer group  to which a peer intends to connect. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>,<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergrouppasswordjoin">PeerGroupPasswordJoin</a> function. This parameter is required.

## -returns

Returns S_OK if the operation succeeds. Otherwise, the function returns  the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

An application  registers for peer events before calling this function. If the function call is unsuccessful, a PEER_GROUP_EVENT_CONNECTION_FAILED event is raised. Otherwise, a PEER_GROUP_EVENT_STATUS_CHANGED event is raised.

The PEER_GROUP_EVENT_CONNECTION_FAILED event is also raised when a group creator fails to call <b>PeerGroupConnect</b> immediately after creation. If this does not take place, users given an invitation will call <b>PeerGroupConnect</b> successfully but they will not be able to listen and will eventually receive the connection failed event.

In the event of a clock skew between participating machines, the success of <b>PeerGroupConnect</b> may depend on the severity of the skew. When troubleshooting a failure to join, this possibility should be taken into consideration by verifying that the machine clocks are synchronized.

To be present in the peer group and receive events but remain unconnected, use the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a> 
	 function.

If a time-out value for <b>PeerGroupConnect</b> is not provided in the application, encountering a failure will cause the application to hang.  A time-out value  of 30 seconds is recommended.

Prior to calling <b>PeerGroupConnect</b>, a group exists in a '<b>Disconnected State</b>'. During this time the group cannot be detected or receive connections. In order  to return a group to this state, the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupclose">PeerGroupClose</a> function must be called.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupclose">PeerGroupClose</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergrouppasswordjoin">PeerGroupPasswordJoin</a>