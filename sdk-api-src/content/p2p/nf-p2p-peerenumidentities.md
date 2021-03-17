---
UID: NF:p2p.PeerEnumIdentities
title: PeerEnumIdentities function (p2p.h)
description: The PeerEnumIdentities function creates and returns a peer enumeration handle used to enumerate all the peer identities that belong to a specific user.
helpviewer_keywords: ["PeerEnumIdentities","PeerEnumIdentities function [Peer Networking]","p2p.peerenumidentities","p2p/PeerEnumIdentities"]
old-location: p2p\peerenumidentities.htm
tech.root: p2p
ms.assetid: 91f18185-0292-41a3-8aff-8b345cab5e82
ms.date: 12/05/2018
ms.keywords: PeerEnumIdentities, PeerEnumIdentities function [Peer Networking], p2p.peerenumidentities, p2p/PeerEnumIdentities
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
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
 - PeerEnumIdentities
 - p2p/PeerEnumIdentities
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
 - PeerEnumIdentities
---

# PeerEnumIdentities function


## -description

The <b>PeerEnumIdentities</b> function creates and returns a peer enumeration handle used to enumerate all the peer identities that belong to a specific user.

## -parameters

### -param phPeerEnum [out]

 Receives a handle to the peer enumeration that contains the list of peer identities, with each item represented as a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_name_pair">PEER_NAME_PAIR</a> structure. Pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> to retrieve the items; when finished, call <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>  to release the memory.

## -returns

If the function call succeeds, the return value is S_OK. Otherwise, it  returns one of the following values.

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

Once the application has obtained the peer enumeration handle, use <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> and <a href="/windows/desktop/api/p2p/nf-p2p-peergetitemcount">PeerGetItemCount</a> to enumerate the peer identities.

When enumerating peer identities, <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>  returns an array of pointers to <a href="/windows/desktop/api/p2p/ns-p2p-peer_name_pair">PEER_NAME_PAIR</a> structures.

Call <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a> to free the enumeration handle when it is no longer required.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_name_pair">PEER_NAME_PAIR</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetitemcount">PeerGetItemCount</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>