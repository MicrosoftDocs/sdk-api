---
UID: NF:p2p.PeerGraphSetPresence
title: PeerGraphSetPresence function (p2p.h)
author: windows-sdk-content
description: The PeerGraphSetPresence function explicitly turns on or off the publication of presence records for a specific node.
old-location: p2p\peergraphsetpresence.htm
tech.root: P2PSdk
ms.assetid: f9d34fb0-4834-4fcf-ab44-e16c8114a3f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGraphSetPresence, PeerGraphSetPresence function [Peer Networking], p2p.peergraphsetpresence, p2p/PeerGraphSetPresence
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
 - PeerGraphSetPresence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphSetPresence function


## -description


The <b>PeerGraphSetPresence</b> function explicitly turns on or off the publication of presence records for a specific  node. This function can override the presence settings in the peer graph properties. Calling this function enables nodes to be enumerated with <a href="https://msdn.microsoft.com/68231b0a-6002-4974-84d7-08b0629f3622">PeerGraphEnumNodes</a>.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param fPresent [in]

Specify <b>TRUE</b> to force the Peer Graphing Infrastructure to publish a presence record for this node, which overrides the setting specified by the <b>cPresenceMax</b> in <a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a>. Specify <b>FALSE</b> to return the node to the default behavior specified in the peer graph properties.

<div class="alert"><b>Note</b>  Depending on the peer graphing presence policy, setting <i>fPresent</i> to <b>FALSE</b> does not guarantee that a peer's presence information is removed. It means that a peer's presence is not published anymore.</div>
<div> </div>

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
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid. The presence information cannot be published.

</td>
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



If presence information has not been explicitly published by the peer graph,  the nodes are not visible when a peer graph is enumerated.  




## -see-also




<a href="https://msdn.microsoft.com/68231b0a-6002-4974-84d7-08b0629f3622">PeerGraphEnumNodes</a>
 

 

