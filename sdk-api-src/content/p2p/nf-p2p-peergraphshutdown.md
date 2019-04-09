---
UID: NF:p2p.PeerGraphShutdown
title: PeerGraphShutdown function (p2p.h)
author: windows-sdk-content
description: The PeerGraphShutdown function cleans up any resources allocated by the call to PeerGraphStartup. There must be a call to PeerGraphShutdown for each call to PeerGraphStartup.
old-location: p2p\peergraphshutdown.htm
tech.root: P2PSdk
ms.assetid: 036f1bd6-f8aa-47ba-841e-f731ff486860
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGraphShutdown, PeerGraphShutdown function [Peer Networking], p2p.peergraphshutdown, p2p/PeerGraphShutdown
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphShutdown function


## -description


The <b>PeerGraphShutdown</b> function cleans up any resources allocated by the call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>.  There must be a call to <b>PeerGraphShutdown</b> for each call to <b>PeerGraphStartup</b>.


## -parameters






## -returns



Returns S_OK if the operation succeeds; otherwise, the function returns the one of the standard error codes defined in WinError.h, or the function returns the following value:

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
The peer graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



When the last <b>PeerGraphShutdown</b> is called for a peer graph, all the opened peer graphs, outstanding enumeration handles, and  outstanding event registration handles are automatically released.




## -see-also




<a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>
 

 

