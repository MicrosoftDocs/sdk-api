---
UID: NF:p2p.PeerGroupClose
title: PeerGroupClose function (p2p.h)
author: windows-sdk-content
description: The PeerGroupClose function invalidates the peer group handle obtained by a previous call to the PeerGroupCreate, PeerGroupJoin, or PeerGroupOpen function.
old-location: p2p\peergroupclose.htm
tech.root: P2PSdk
ms.assetid: 4438e6c1-8c25-4656-bac5-dda43421ee43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGroupClose, PeerGroupClose function [Peer Networking], p2p.peergroupclose, p2p/PeerGroupClose
ms.topic: function
f1_keywords: 
 - "p2p/PeerGroupClose"
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
 - PeerGroupClose
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerGroupClose function


## -description


The <b>PeerGroupClose</b> function invalidates the peer group handle obtained by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a> function. 


## -parameters




### -param hGroup [in]

Handle to the peer group to close. This handle is returned by the  <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.


## -returns



Returns S_OK if the operation succeeds. Otherwise, the function returns the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



If the peer group handle closed is the last handle that refers to a peer group shared  across multiple applications or processes, the call  also closes the respective network connections  for the peer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>
 

 

