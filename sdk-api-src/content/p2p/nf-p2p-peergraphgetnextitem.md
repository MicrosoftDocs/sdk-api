---
UID: NF:p2p.PeerGraphGetNextItem
title: PeerGraphGetNextItem function (p2p.h)
description: Obtains the next item or items in an enumeration created by a call to the following functions.
helpviewer_keywords: ["PeerGraphGetNextItem","PeerGraphGetNextItem function [Peer Networking]","p2p.peergraphgetnextitem","p2p/PeerGraphGetNextItem"]
old-location: p2p\peergraphgetnextitem.htm
tech.root: p2p
ms.assetid: f595e66d-570f-4642-bef8-ff5cf070649c
ms.date: 12/05/2018
ms.keywords: PeerGraphGetNextItem, PeerGraphGetNextItem function [Peer Networking], p2p.peergraphgetnextitem, p2p/PeerGraphGetNextItem
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
 - PeerGraphGetNextItem
 - p2p/PeerGraphGetNextItem
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
 - PeerGraphGetNextItem
---

# PeerGraphGetNextItem function


## -description

The <b>PeerGraphGetNextItem</b> function obtains the next item or items in an enumeration created by a call to the following functions, which return a peer enumeration handle:  <ul>
<li>
<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>
</li>
<li>
<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumnodes">PeerGraphEnumNodes</a>
</li>
<li>
<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>
</li>
<li>
<a href="/windows/desktop/api/p2p/nf-p2p-peergraphsearchrecords">PeerGraphSearchRecords</a>
</li>
</ul>

## -parameters

### -param hPeerEnum [in]

Handle to an enumeration.

### -param pCount [in, out]

Input specifies the number of items to obtain.

Output receives the actual number of items obtained.

<div class="alert"><b>Note</b>  If <i>pCount</i> is a zero (0) output, the end of the enumeration is reached.</div>
<div> </div>

### -param pppvItems [out]

Receives an array of pointers to  the requested items.  The number  of pointers contained in an array is specified by the output value of  <i>pCount</i>.  The actual data returned depends on the type of enumeration. The  types of structures that are returned are the following:  <a href="/windows/desktop/api/p2p/ns-p2p-peer_connection_info">PEER_CONNECTION_INFO</a>, <a href="/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a>, and <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>

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
One parameter is not valid.

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
The graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

 Free  <i>ppvItems</i> by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a> when the data is no longer required.

The application can request a range of items to obtain.   The function  returns <i>pCount</i> or fewer items.


#### Examples

The following code snippet shows you how to  use  <b>PeerGraphGetNextItem</b> to enumerate objects, and end an enumeration after you finish processing the enumeration.


```cpp
//PeerGraphGetNextItem snippet
    // hPeerEnum is a handle to the enumeration obtained from a successful call to PeerGraphEnumConnections,
    // PeerGraphEnumNodes, PeerGraphEnumRecords, or PeerGraphSearchRecords.
    // Set count equal to the maximum number of items you want returned. To obtain a count of all the items
    // in the enumeration, call PeerGraphGetItemCount.
    // ppRecord is an array of pointers to PEER_RECORD objects.  PEER_CONNECTION_INFO and PEER_NODE_INFO structures
    // are also supported.
    HRESULT hr = PeerGraphGetNextItem(hPeerEnum, &count, (PVOID *)&ppRecord);
    if (FAILED(hr))
    {
        // Insert your code to handle the error here.
    }
    else
    {
        // Free the data obtained by PeerGraphGetNextItem.
        PeerGraphFreeData(ppRecord);
    }

    // If you are done with the enumeration, free the handle to the enumeration.
    PeerGraphEndEnumeration(hPeerEnum);

```

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_connection_info">PEER_CONNECTION_INFO</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumnodes">PeerGraphEnumNodes</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphsearchrecords">PeerGraphSearchRecords</a>