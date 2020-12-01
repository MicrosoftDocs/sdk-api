---
UID: NF:p2p.PeerIdentitySetFriendlyName
title: PeerIdentitySetFriendlyName function (p2p.h)
description: The PeerIdentitySetFriendlyName function modifies the friendly name for a specified peer identity. The friendly name is the human-readable name.
helpviewer_keywords: ["PeerIdentitySetFriendlyName","PeerIdentitySetFriendlyName function [Peer Networking]","p2p.peeridentitysetfriendlyname","p2p/PeerIdentitySetFriendlyName"]
old-location: p2p\peeridentitysetfriendlyname.htm
tech.root: p2p
ms.assetid: 018e95b5-b817-44f8-909f-cc7c3edb84c8
ms.date: 12/05/2018
ms.keywords: PeerIdentitySetFriendlyName, PeerIdentitySetFriendlyName function [Peer Networking], p2p.peeridentitysetfriendlyname, p2p/PeerIdentitySetFriendlyName
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
 - PeerIdentitySetFriendlyName
 - p2p/PeerIdentitySetFriendlyName
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
 - PeerIdentitySetFriendlyName
---

# PeerIdentitySetFriendlyName function


## -description

The <b>PeerIdentitySetFriendlyName</b> function modifies the  friendly name for a specified peer identity. The friendly name is the human-readable name.

## -parameters

### -param pwzIdentity [in]

Specifies a peer identity to modify.

### -param pwzFriendlyName [in]

Specifies a new friendly name. Specify <b>NULL</b> or an empty string to reset a friendly name to the default value, which is the Unicode version of the peer name.

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
Access to the peer identity or peer group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A peer identity that matches a specified name cannot be found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peeridentitygetfriendlyname">PeerIdentityGetFriendlyName</a>