---
UID: NF:p2p.PeerGroupStartup
title: PeerGroupStartup function (p2p.h)
description: The PeerGroupStartup function initiates a peer group by using a requested version of the Peer infrastructure.
helpviewer_keywords: ["PeerGroupStartup","PeerGroupStartup function [Peer Networking]","p2p.peergroupstartup","p2p/PeerGroupStartup"]
old-location: p2p\peergroupstartup.htm
tech.root: p2p
ms.assetid: c07e200d-9578-4367-a0f8-699ae300fc1f
ms.date: 12/05/2018
ms.keywords: PeerGroupStartup, PeerGroupStartup function [Peer Networking], p2p.peergroupstartup, p2p/PeerGroupStartup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGroupStartup
 - p2p/PeerGroupStartup
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
 - PeerGroupStartup
---

# PeerGroupStartup function


## -description

The <b>PeerGroupStartup</b> function initiates a peer group by using a requested version of the Peer infrastructure.

## -parameters

### -param wVersionRequested [in]

Specifies the highest version of the Peer Infrastructure that a caller can support. The high order byte specifies the minor version (revision) number.  The low order byte specifies the major version number This parameter is required.

### -param pVersionData [out]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_version_data">PEER_VERSION_DATA</a> structure that contains the specific level of support provided by the Peer Infrastructure. This parameter is required.

## -returns

Returns <b>S_OK</b> if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DEPENDENCY_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/P2PSdk/pnrp-namespace-provider-api">Peer Name Resolution Protocol (PNRP)</a> service must be started before calling <a href="/windows/desktop/api/p2p/nf-p2p-peergroupstartup">PeerGroupStartup</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_IPV6_NOT_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The grouping service failed to start because IPv6 is not installed on the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The requested version is not supported by the installed Peer subsystem.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

The   <a href="/windows/desktop/P2PSdk/pnrp-namespace-provider-api">Peer Name Resolution Protocol (PNRP)</a> service must be started before calling this function.

This function is called by the application before calling any other Peer Grouping function.

For this release, applications should use <b>PEER_GROUP_VERSION</b> as the requested version.

A peer group started with this function is closed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergroupshutdown">PeerGroupShutdown</a> when the application terminates.

## -see-also

<a href="/windows/desktop/P2PSdk/grouping-api-functions">Grouping API Functions</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_version_data">PEER_VERSION_DATA</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupshutdown">PeerGroupShutdown</a>