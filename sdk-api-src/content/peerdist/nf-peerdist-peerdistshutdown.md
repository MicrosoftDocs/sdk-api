---
UID: NF:peerdist.PeerDistShutdown
title: PeerDistShutdown function (peerdist.h)
description: PeerDistShutdown function releases resources allocated by a call to PeerDistStartup. Each handle returned by a PeerDistStartup call must be closed by a matching call to PeerDistShutdown.
helpviewer_keywords: ["PeerDistShutdown","PeerDistShutdown function [Peer Networking]","p2p.peerdistshutdown","peerdist/PeerDistShutdown"]
old-location: p2p\peerdistshutdown.htm
tech.root: p2p
ms.assetid: 47fe4a77-2895-4d5b-beff-995e12fb0644
ms.date: 12/05/2018
ms.keywords: PeerDistShutdown, PeerDistShutdown function [Peer Networking], p2p.peerdistshutdown, peerdist/PeerDistShutdown
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
 - PeerDistShutdown
 - peerdist/PeerDistShutdown
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
 - PeerDistShutdown
---

# PeerDistShutdown function


## -description

The <b>PeerDistShutdown</b> function releases resources allocated by a call to <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>. Each handle returned by a <b>PeerDistStartup</b> call must be closed by a matching call to <b>PeerDistShutdown</b>

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned  by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPeerDist</i> handle is invalid.

</td>
</tr>
</table>

## -remarks

 
This function will remove all publications that were created  with the specified <i>hPeerDist</i> handle. It is recommended that this function is called after all pending operations have completed, as <b>PeerDistShutdown</b> cancel all pending Peer Distribution client and server operations associated with the supplied <b>PEERDIST_INSTANCE_HANDLE</b>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>