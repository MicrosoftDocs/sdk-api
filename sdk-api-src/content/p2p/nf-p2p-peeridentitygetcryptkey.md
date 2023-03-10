---
UID: NF:p2p.PeerIdentityGetCryptKey
title: PeerIdentityGetCryptKey function (p2p.h)
description: The PeerIdentityGetCryptKey function retrieves a handle to a cryptographic service provider (CSP).
helpviewer_keywords: ["PeerIdentityGetCryptKey","PeerIdentityGetCryptKey function [Peer Networking]","p2p.peeridentitygetcryptkey","p2p/PeerIdentityGetCryptKey"]
old-location: p2p\peeridentitygetcryptkey.htm
tech.root: p2p
ms.assetid: 27a1b563-7bbe-4117-8bc3-19dd47360308
ms.date: 12/05/2018
ms.keywords: PeerIdentityGetCryptKey, PeerIdentityGetCryptKey function [Peer Networking], p2p.peeridentitygetcryptkey, p2p/PeerIdentityGetCryptKey
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
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
 - PeerIdentityGetCryptKey
 - p2p/PeerIdentityGetCryptKey
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
 - PeerIdentityGetCryptKey
---

# PeerIdentityGetCryptKey function


## -description

The <b>PeerIdentityGetCryptKey</b> function retrieves a handle to a cryptographic service provider (CSP).

## -parameters

### -param pwzIdentity [in]

Specifies the peer identity to retrieve the key pair for.

### -param phCryptProv [out]

Receives a pointer to the handle of the  cryptographic service provider (CSP) that contains an AT_KEYEXCHANGE RSA key pair.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been manually reset. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An identity that matches the specified name cannot be found.

</td>
</tr>
</table>

## -remarks

The  key can be retrieved by calling <a href="/windows/desktop/P2PSdk/identity-manager-reference-links">CryptGetUserKey</a>.

When the handle is not required anymore, the application is responsible for releasing the handle by using <a href="/windows/desktop/P2PSdk/identity-manager-reference-links">CryptReleaseContext</a>.

## -see-also

<a href="/windows/desktop/P2PSdk/identity-manager-reference-links">CryptGetUserKey</a>



CryptReleaseContext