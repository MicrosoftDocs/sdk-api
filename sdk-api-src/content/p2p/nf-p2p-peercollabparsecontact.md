---
UID: NF:p2p.PeerCollabParseContact
title: PeerCollabParseContact function (p2p.h)
description: Parses a Unicode string buffer containing contact XML data into a PEER_CONTACT data structure.
helpviewer_keywords: ["PeerCollabParseContact","PeerCollabParseContact function [Peer Networking]","p2p.peercollabparsecontact","p2p/PeerCollabParseContact"]
old-location: p2p\peercollabparsecontact.htm
tech.root: p2p
ms.assetid: c50954b2-0e63-412e-85ca-5149ed73791f
ms.date: 12/05/2018
ms.keywords: PeerCollabParseContact, PeerCollabParseContact function [Peer Networking], p2p.peercollabparsecontact, p2p/PeerCollabParseContact
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - PeerCollabParseContact
 - p2p/PeerCollabParseContact
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
 - PeerCollabParseContact
---

# PeerCollabParseContact function


## -description

The <b>PeerCollabParseContact</b> function parses a Unicode string buffer containing contact XML data into a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> data structure.

## -parameters

### -param pwzContactData [in]

Pointer to zero-terminated Unicode string buffer that contains XML contact data as returned by functions like <a href="/windows/desktop/api/p2p/nf-p2p-peercollabquerycontactdata">PeerCollabQueryContactData</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peercollabexportcontact">PeerCollabExportContact</a>.

### -param ppContact [out]

Pointer to the address of a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contain the peer contact information parsed from <i>pwzContactData</i>. Free the memory allocated by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

## -returns

Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>