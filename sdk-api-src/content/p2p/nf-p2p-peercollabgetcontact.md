---
UID: NF:p2p.PeerCollabGetContact
title: PeerCollabGetContact function (p2p.h)
author: windows-sdk-content
description: Obtains the information for a peer contact given the peer name of the contact.
old-location: p2p\peercollabgetcontact.htm
tech.root: P2PSdk
ms.assetid: b1233942-1bd5-4198-a00c-6d0516ab32dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerCollabGetContact, PeerCollabGetContact function [Peer Networking], p2p.peercollabgetcontact, p2p/PeerCollabGetContact
ms.topic: function
f1_keywords: 
 - "p2p/PeerCollabGetContact"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabGetContact
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerCollabGetContact function


## -description


The <b>PeerCollabGetContact</b> function obtains the information for a peer contact given the peer name of the contact.


## -parameters




### -param pwzPeerName [in, optional]

Pointer to zero-terminated Unicode string that contains the name of the peer contact for which to obtain information. 

If this parameter is <b>NULL</b>, the 'Me' contact information for the calling peer is returned.


### -param ppContact [out, optional]

Pointer to a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure. It receives the address of a PEER_CONTACT structure containing peer contact information for the peer name supplied in <i>pwzPeerName</i>. When this parameter is <b>NULL</b>, this function returns E_INVALIDARG.

Call <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a> on the address of the <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure to free this data.


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




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="https://docs.microsoft.com/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>
 

 

