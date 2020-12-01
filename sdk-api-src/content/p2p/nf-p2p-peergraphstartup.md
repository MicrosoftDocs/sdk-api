---
UID: NF:p2p.PeerGraphStartup
title: PeerGraphStartup function (p2p.h)
description: The PeerGraphStartup function indicates to the Peer Graphing Infrastructure what version of the Peer protocols the calling application requires.
helpviewer_keywords: ["PeerGraphStartup","PeerGraphStartup function [Peer Networking]","p2p.peergraphstartup","p2p/PeerGraphStartup"]
old-location: p2p\peergraphstartup.htm
tech.root: p2p
ms.assetid: 00ffdec7-f084-4170-a4a1-e6112bab4d61
ms.date: 12/05/2018
ms.keywords: PeerGraphStartup, PeerGraphStartup function [Peer Networking], p2p.peergraphstartup, p2p/PeerGraphStartup
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGraphStartup
 - p2p/PeerGraphStartup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphStartup
---

# PeerGraphStartup function


## -description

The <b>PeerGraphStartup</b> function  indicates to the Peer Graphing Infrastructure what version of the Peer protocols the calling application requires.  <b>PeerGraphStartup</b> must be called before any other peer graphing functions. It must be matched by a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphshutdown">PeerGraphShutdown</a>.

## -parameters

### -param wVersionRequested [in]

Specify PEER_GRAPH_VERSION.

### -param pVersionData [out]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_version_data">PEER_VERSION_DATA</a> structure that receives the 
version of the Peer Infrastructure installed on the local computer.

## -returns

Returns S_OK if the operation succeeds; otherwise, the function returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The version requested is not supported by the Peer Infrastructure .dll installed on the local computer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_version_data">PEER_VERSION_DATA</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphshutdown">PeerGraphShutdown</a>