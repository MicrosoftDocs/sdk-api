---
UID: NF:p2p.PeerGraphStartup
title: PeerGraphStartup function
author: windows-driver-content
description: The PeerGraphStartup function indicates to the Peer Graphing Infrastructure what version of the Peer protocols the calling application requires.
old-location: p2p\peergraphstartup.htm
old-project: P2PSdk
ms.assetid: 00ffdec7-f084-4170-a4a1-e6112bab4d61
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PeerGraphStartup, PeerGraphStartup function [Peer Networking], p2p.peergraphstartup, p2p/PeerGraphStartup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2PGraph.dll
api_name:
-	PeerGraphStartup
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PeerGraphStartup function


## -description



      The <b>PeerGraphStartup</b> function  indicates to the Peer Graphing Infrastructure what version of the Peer protocols the calling application requires.  <b>PeerGraphStartup</b> must be called before any other peer graphing functions. It must be matched by a call to <a href="https://msdn.microsoft.com/036f1bd6-f8aa-47ba-841e-f731ff486860">PeerGraphShutdown</a>.


## -parameters




### -param wVersionRequested [in]

Specify PEER_GRAPH_VERSION.


### -param pVersionData [out]

Pointer to a <a href="https://msdn.microsoft.com/b212101f-8c34-41d1-92b9-4daf3591200e">PEER_VERSION_DATA</a> structure that receives the 
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




<a href="https://msdn.microsoft.com/b212101f-8c34-41d1-92b9-4daf3591200e">
        PEER_VERSION_DATA</a>



<a href="https://msdn.microsoft.com/036f1bd6-f8aa-47ba-841e-f731ff486860">PeerGraphShutdown</a>
 

 

