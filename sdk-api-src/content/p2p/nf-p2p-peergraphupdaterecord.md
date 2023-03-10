---
UID: NF:p2p.PeerGraphUpdateRecord
title: PeerGraphUpdateRecord function (p2p.h)
description: The PeerGraphUpdateRecord function updates a record in the peer graph and then floods the record to each node in the peer graph.
helpviewer_keywords: ["PeerGraphUpdateRecord","PeerGraphUpdateRecord function [Peer Networking]","p2p.peergraphupdaterecord","p2p/PeerGraphUpdateRecord"]
old-location: p2p\peergraphupdaterecord.htm
tech.root: p2p
ms.assetid: 9007095f-4f2a-4e92-895b-9a4033f0f7b9
ms.date: 12/05/2018
ms.keywords: PeerGraphUpdateRecord, PeerGraphUpdateRecord function [Peer Networking], p2p.peergraphupdaterecord, p2p/PeerGraphUpdateRecord
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
 - PeerGraphUpdateRecord
 - p2p/PeerGraphUpdateRecord
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
 - PeerGraphUpdateRecord
---

# PeerGraphUpdateRecord function


## -description

The <b>PeerGraphUpdateRecord</b> function updates a record in the peer graph and then floods the record to each node in the peer graph.

## -parameters

### -param hGraph [in]

Handle to the peer graph.

### -param pRecord [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a> structure that contains the  new data for the record.

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
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer graph has never been synchronized. Records cannot be updated until the graph has been synchronized.

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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record was not found.

</td>
</tr>
</table>

## -remarks

The following members of the  <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a> structure can be modified:

<ul>
<li><b>pwzAttributes</b></li>
<li><b>ftExpiration</b> - the expiration can only be increased</li>
<li><b>data</b></li>
<li><b>pwzLastModified</b> - filled in by default if no value is supplied</li>
</ul>

#### Examples

This code snippet shows how to update a record.


```cpp
// dwFlags is updated to automatically refresh the record if it is about to expire.
    record.dwFlags = PEER_RECORD_FLAG_AUTOREFRESH;
    // The record data is updated with the string contained in pwzUserData.
    record.data.cbData = (ULONG) wcslen(pwzUserData) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzUserData;

    HRESULT hr = PeerGraphUpdateRecord(hGraph, &record;);

    if (FAILED(hr))
    {
        // Insert your code to handle the error here.
    }
    else
    {
        // Insert your application specific code here.
    }

```

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>