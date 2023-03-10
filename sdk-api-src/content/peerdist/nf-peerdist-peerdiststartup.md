---
UID: NF:peerdist.PeerDistStartup
title: PeerDistStartup function (peerdist.h)
description: PeerDistStartup function creates a new Peer Distribution instance handle which must be passed to all other Peer Distribution APIs.
helpviewer_keywords: ["PeerDistStartup","PeerDistStartup function [Peer Networking]","p2p.peerdiststartup","peerdist/PeerDistStartup"]
old-location: p2p\peerdiststartup.htm
tech.root: p2p
ms.assetid: 62d4f139-ab18-4d65-bda5-1cf09d7ddab9
ms.date: 12/05/2018
ms.keywords: PeerDistStartup, PeerDistStartup function [Peer Networking], p2p.peerdiststartup, peerdist/PeerDistStartup
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistStartup
 - peerdist/PeerDistStartup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistStartup
---

# PeerDistStartup function


## -description

The <b>PeerDistStartup</b> function creates a new Peer Distribution instance handle which must be passed to all other Peer Distribution APIs.

## -parameters

### -param dwVersionRequested [in]

Contains the minimum version of the Peer Distribution requested by the application. The high order byte specifies the minor version number; the low order byte specifies the major version number.

### -param phPeerDist [out]

A pointer to a <b>PEERDIST_INSTANCE_HANDLE</b> variable which upon success receives a newly created handle.

### -param pdwSupportedVersion [out, optional]

A pointer to a variable which, if not <b>NULL</b>, contains the maximum version number that is supported by the Peer Distribution system. The high order byte specifies the minor version number; the low order byte specifies the major version number.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_VERSION_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested version is not supported by client side DLL.

</td>
</tr>
</table>

## -remarks

<b>PeerDistStartup</b> must be called before any other Peer Distribution functions. When no longer needed, the handle returned by <b>PeerDistStartup</b> should be closed via a call to <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistshutdown">PeerDistShutdown</a>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistshutdown">PeerDistShutdown</a>