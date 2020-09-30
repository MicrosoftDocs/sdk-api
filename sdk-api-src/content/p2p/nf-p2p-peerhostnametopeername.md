---
UID: NF:p2p.PeerHostNameToPeerName
title: PeerHostNameToPeerName function (p2p.h)
description: Decodes a host name returned by PeerNameToPeerHostName into the peer name string it represents.
helpviewer_keywords: ["PeerHostNameToPeerName","PeerHostNameToPeerName function [Peer Networking]","p2p.peerhostnametopeername","p2p/PeerHostNameToPeerName"]
old-location: p2p\peerhostnametopeername.htm
tech.root: p2p
ms.assetid: 3150d37e-84a3-4386-b38c-b37f7d6642cc
ms.date: 12/05/2018
ms.keywords: PeerHostNameToPeerName, PeerHostNameToPeerName function [Peer Networking], p2p.peerhostnametopeername, p2p/PeerHostNameToPeerName
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PeerHostNameToPeerName
 - p2p/PeerHostNameToPeerName
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
 - PeerHostNameToPeerName
---

# PeerHostNameToPeerName function


## -description

The <b>PeerHostNameToPeerName</b> function decodes a host name returned by <a href="/windows/desktop/api/p2p/nf-p2p-peernametopeerhostname">PeerNameToPeerHostName</a> into the peer name string it represents.

## -parameters

### -param pwzHostName [in]

Pointer to a zero-terminated Unicode string that contains the host name to decode.

### -param ppwzPeerName [out]

Pointer to the address of the zero-terminated Unicode string that contains the decoded peer name. The returned  string must be released with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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

<a href="/windows/desktop/api/p2p/nf-p2p-peernametopeerhostname">PeerNameToPeerHostName</a>