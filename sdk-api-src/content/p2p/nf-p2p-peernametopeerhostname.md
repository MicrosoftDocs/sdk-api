---
UID: NF:p2p.PeerNameToPeerHostName
title: PeerNameToPeerHostName function
author: windows-sdk-content
description: Encodes the supplied peer name as a format that can be used with a subsequent call to the getaddrinfo Windows Sockets function.
old-location: p2p\peernametopeerhostname.htm
old-project: p2psdk
ms.assetid: 430ff635-8c45-44d1-bced-d075faf2bd30
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerNameToPeerHostName, PeerNameToPeerHostName function [Peer Networking], p2p.peernametopeerhostname, p2p/PeerNameToPeerHostName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerNameToPeerHostName
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerNameToPeerHostName function


## -description


The <b>PeerNameToPeerHostName</b> function encodes the supplied peer name as a format that can be used with a subsequent call to the <a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a> Windows Sockets function.


## -parameters




### -param pwzPeerName [in]

Pointer to a zero-terminated Unicode string that contains the peer name to encode as a host name.


### -param ppwzHostName [out]

Pointer to the address of the zero-terminated Unicode string that contains the encoded host name. This string can be passed to <a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo_v2</a> to obtain network information about the peer.


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




<a href="https://msdn.microsoft.com/3150d37e-84a3-4386-b38c-b37f7d6642cc">PeerHostNameToPeerName</a>
 

 

