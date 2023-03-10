---
UID: NF:p2p.PeerNameToPeerHostName
title: PeerNameToPeerHostName function (p2p.h)
description: Encodes the supplied peer name as a format that can be used with a subsequent call to the getaddrinfo Windows Sockets function.
helpviewer_keywords: ["PeerNameToPeerHostName","PeerNameToPeerHostName function [Peer Networking]","p2p.peernametopeerhostname","p2p/PeerNameToPeerHostName"]
old-location: p2p\peernametopeerhostname.htm
tech.root: p2p
ms.assetid: 430ff635-8c45-44d1-bced-d075faf2bd30
ms.date: 12/05/2018
ms.keywords: PeerNameToPeerHostName, PeerNameToPeerHostName function [Peer Networking], p2p.peernametopeerhostname, p2p/PeerNameToPeerHostName
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
 - PeerNameToPeerHostName
 - p2p/PeerNameToPeerHostName
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
 - PeerNameToPeerHostName
---

# PeerNameToPeerHostName function


## -description

The <b>PeerNameToPeerHostName</b> function encodes the supplied peer name as a format that can be used with a subsequent call to the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> Windows Sockets function.

## -parameters

### -param pwzPeerName [in]

Pointer to a zero-terminated Unicode string that contains the peer name to encode as a host name.

### -param ppwzHostName [out]

Pointer to the address of the zero-terminated Unicode string that contains the encoded host name. This string can be passed to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo_v2</a> to obtain network information about the peer.

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

<a href="/windows/desktop/api/p2p/nf-p2p-peerhostnametopeername">PeerHostNameToPeerName</a>