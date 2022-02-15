---
UID: NF:p2p.PeerPnrpShutdown
title: PeerPnrpShutdown function (p2p.h)
description: Shuts down a running instance of the Peer Name Resolution Protocol (PNRP) service and releases all resources associated with it.
helpviewer_keywords: ["PeerPnrpShutdown","PeerPnrpShutdown function [Peer Networking]","p2p.peerpnrpshutdown","p2p/PeerPnrpShutdown"]
old-location: p2p\peerpnrpshutdown.htm
tech.root: p2p
ms.assetid: e617fb5b-ace2-46b4-b165-4cd9cf891ac7
ms.date: 12/05/2018
ms.keywords: PeerPnrpShutdown, PeerPnrpShutdown function [Peer Networking], p2p.peerpnrpshutdown, p2p/PeerPnrpShutdown
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
 - PeerPnrpShutdown
 - p2p/PeerPnrpShutdown
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
 - PeerPnrpShutdown
---

# PeerPnrpShutdown function


## -description

The <b>PeerPnrpShutdown</b> function shuts down a running instance of the Peer Name Resolution Protocol (PNRP) service and releases all resources associated with it.



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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

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

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartup">PeerPnrpStartup</a>
