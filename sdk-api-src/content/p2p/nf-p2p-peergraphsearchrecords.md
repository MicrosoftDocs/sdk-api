---
UID: NF:p2p.PeerGraphSearchRecords
title: PeerGraphSearchRecords function (p2p.h)
description: The PeerGraphSearchRecords function searches the peer graph for specific records.
helpviewer_keywords: ["PeerGraphSearchRecords","PeerGraphSearchRecords function [Peer Networking]","p2p.peergraphsearchrecords","p2p/PeerGraphSearchRecords"]
old-location: p2p\peergraphsearchrecords.htm
tech.root: p2p
ms.assetid: 0f20c738-ae56-4352-a1fb-5aa469a58bc8
ms.date: 12/05/2018
ms.keywords: PeerGraphSearchRecords, PeerGraphSearchRecords function [Peer Networking], p2p.peergraphsearchrecords, p2p/PeerGraphSearchRecords
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
 - PeerGraphSearchRecords
 - p2p/PeerGraphSearchRecords
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
 - PeerGraphSearchRecords
---

# PeerGraphSearchRecords function


## -description

The <b>PeerGraphSearchRecords</b> function searches the peer graph for specific records.

## -parameters

### -param hGraph [in]

Handle to the peer graph.

### -param pwzCriteria [in]

Pointer to an XML string that specifies the records to search for. For information on formulating an XML query string to search the peer graphing records, see <a href="/windows/desktop/P2PSdk/record-search-query-format">Record Search Query Format</a>.

### -param phPeerEnum [out]

Handle to the enumeration.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_SEARCH</b></dt>
</dl>
</td>
<td width="60%">
The specified query does not adhere to the search schema.  See <a href="/windows/desktop/P2PSdk/record-search-query-format">Record Search Query Format</a> for further information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a> function is more efficient than the  <b>PeerGraphSearchRecords</b> function.

When <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a> is called with the handle returned by  <b>PeerGraphSearchRecords</b>, <b>PeerGraphGetNextItem</b>  returns the data in the  <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a> structure.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetitemcount">PeerGraphGetItemCount</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a>