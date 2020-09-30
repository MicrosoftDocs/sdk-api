---
UID: NF:p2p.PeerGetItemCount
title: PeerGetItemCount function (p2p.h)
description: The PeerGetItemCount function returns a count of the items in a peer enumeration.
helpviewer_keywords: ["PeerGetItemCount","PeerGetItemCount function [Peer Networking]","p2p.peergetitemcount","p2p/PeerGetItemCount"]
old-location: p2p\peergetitemcount.htm
tech.root: p2p
ms.assetid: 8f6fec31-8867-4d65-b5b0-e6506be9c991
ms.date: 12/05/2018
ms.keywords: PeerGetItemCount, PeerGetItemCount function [Peer Networking], p2p.peergetitemcount, p2p/PeerGetItemCount
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
 - PeerGetItemCount
 - p2p/PeerGetItemCount
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
 - PeerGetItemCount
---

# PeerGetItemCount function


## -description

The <b>PeerGetItemCount</b> function returns a count of the items  in a peer enumeration.

## -parameters

### -param hPeerEnum [in]

Handle to the peer enumeration on which a count is performed. A peer enumeration function generates this handle.

### -param pCount [out]

Returns the total number of items in a peer enumeration.

## -returns

Returns <b>S_OK</b> if the operation succeeds. Otherwise, the function returns one of the following values.

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

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerenumgroups">PeerEnumGroups</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerenumidentities">PeerEnumIdentities</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupenumconnections">PeerGroupEnumConnections</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupenummembers">PeerGroupEnumMembers</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupenumrecords">PeerGroupEnumRecords</a>