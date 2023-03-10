---
UID: NF:p2p.PeerCreatePeerName
title: PeerCreatePeerName function (p2p.h)
description: The PeerCreatePeerName function creates a new name based on the existing name of the specified peer identity and classifier. However, a new identity is not created by a call to PeerCreatePeerName.
helpviewer_keywords: ["PeerCreatePeerName","PeerCreatePeerName function [Peer Networking]","p2p.peercreatepeername","p2p/PeerCreatePeerName"]
old-location: p2p\peercreatepeername.htm
tech.root: p2p
ms.assetid: 8248b0ae-5d35-4d6e-91ef-c210033c99ef
ms.date: 12/05/2018
ms.keywords: PeerCreatePeerName, PeerCreatePeerName function [Peer Networking], p2p.peercreatepeername, p2p/PeerCreatePeerName
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
 - PeerCreatePeerName
 - p2p/PeerCreatePeerName
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
 - PeerCreatePeerName
---

# PeerCreatePeerName function


## -description

The <b>PeerCreatePeerName</b> function  creates a new name based on the existing name of the specified peer identity and classifier. However, a new identity is not created by a call to <b>PeerCreatePeerName</b>.

## -parameters

### -param pwzIdentity [in]

Specifies the identity to use as the basis for the new peer name. If <i>pwzIdentity</i> is <b>NULL</b>, the name created is not based on any peer identity, and is therefore an unsecured name.

This parameter can only be <b>NULL</b> if <i>pwzClassifier</i> is not <b>NULL</b>.

### -param pwzClassifier [in]

Pointer to the Unicode string that contains the new classifier. This classifier is appended to the existing authority portion of the peer name of the specified identity. This string is 150 characters long, including the <b>NULL</b> terminator. Specify <b>NULL</b> to return the peer name of the identity.  

This parameter can only be <b>NULL</b> if <i>pwzIdentity</i> is not <b>NULL</b>.

### -param ppwzPeerName [out]

Pointer that receives a pointer to the new peer name. When this string is not required anymore, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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

## -remarks

The parameter  <i>ppwzPeername</i> must be set to null before the <b>PeerCreatePeerName</b> function is called.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>