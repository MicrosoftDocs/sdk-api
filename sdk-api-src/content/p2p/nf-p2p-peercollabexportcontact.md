---
UID: NF:p2p.PeerCollabExportContact
title: PeerCollabExportContact function (p2p.h)
description: Exports the contact data associated with a peer name to a string buffer. The buffer contains contact data in XML format.
helpviewer_keywords: ["PeerCollabExportContact","PeerCollabExportContact function [Peer Networking]","p2p.peercollabexportcontact","p2p/PeerCollabExportContact"]
old-location: p2p\peercollabexportcontact.htm
tech.root: p2p
ms.assetid: 8239e42f-3d86-416e-ad1b-93a37091811f
ms.date: 12/05/2018
ms.keywords: PeerCollabExportContact, PeerCollabExportContact function [Peer Networking], p2p.peercollabexportcontact, p2p/PeerCollabExportContact
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
 - PeerCollabExportContact
 - p2p/PeerCollabExportContact
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
 - PeerCollabExportContact
---

# PeerCollabExportContact function


## -description

The <b>PeerCollabExportContact</b> function exports the contact data associated with a peer name to a string buffer. The buffer contains contact data in XML format.

The <a href="/windows/desktop/api/p2p/nf-p2p-peercollabaddcontact">PeerCollabAddContact</a> function allows this XML string to be utilized by other peers.

## -parameters

### -param pwzPeerName [in, optional]

Pointer to zero-terminated Unicode string that contains the name of the peer contact for which to export. 

If this parameter is <b>NULL</b>, the "Me" contact information for the calling peer is exported.

### -param ppwzContactData [out, optional]

Pointer to a zero-terminated string buffer that contains peer contact XML data where the peer names match the string supplied in <i>pwzPeerName</i>.  

The memory returned here can be freed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>