---
UID: NF:p2p.PeerGraphGetItemCount
title: PeerGraphGetItemCount function (p2p.h)
description: The PeerGraphGetItemCount function retrieves the number of items in an enumeration.
helpviewer_keywords: ["PeerGraphGetItemCount","PeerGraphGetItemCount function [Peer Networking]","p2p.peergraphgetitemcount","p2p/PeerGraphGetItemCount"]
old-location: p2p\peergraphgetitemcount.htm
tech.root: p2p
ms.assetid: db97b7e0-6f85-4b61-843f-efb4bc93149b
ms.date: 12/05/2018
ms.keywords: PeerGraphGetItemCount, PeerGraphGetItemCount function [Peer Networking], p2p.peergraphgetitemcount, p2p/PeerGraphGetItemCount
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
 - PeerGraphGetItemCount
 - p2p/PeerGraphGetItemCount
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
 - PeerGraphGetItemCount
---

# PeerGraphGetItemCount function


## -description

The <b>PeerGraphGetItemCount</b> function retrieves the  number of items in an enumeration.

## -parameters

### -param hPeerEnum [in]

Handle to a peer graph.

### -param pCount [out]

Receives a pointer to the number of records in an enumeration.

## -returns

If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns  the following value.

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
One  parameter is not valid.

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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

Because some items can become invalid while an application is enumerating a set of items, the number of items returned from <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a> can be less than the number of items  returned in <i>pCount</i>.  The value of  <i>pCount</i> indicates the number of items in an enumeration when the handle is created.  Due to the dynamic nature of the Peer Infrastructure, it is not guaranteed that the number of items retrieved by using <b>PeerGraphGetNextItem</b> is equal to <i>pCount</i>.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a>