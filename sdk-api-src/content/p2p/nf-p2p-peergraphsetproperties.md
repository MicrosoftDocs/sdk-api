---
UID: NF:p2p.PeerGraphSetProperties
title: PeerGraphSetProperties function (p2p.h)
author: windows-sdk-content
description: The PeerGraphSetProperties function sets the peer graph properties.
old-location: p2p\peergraphsetproperties.htm
tech.root: P2PSdk
ms.assetid: a9cdf715-bbef-4b5b-96b9-b7c1e35c76ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGraphSetProperties, PeerGraphSetProperties function [Peer Networking], p2p.peergraphsetproperties, p2p/PeerGraphSetProperties
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
 - PeerGraphSetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerGraphSetProperties function


## -description


The <b>PeerGraphSetProperties</b> function sets the peer graph properties.


## -parameters




### -param hGraph [in]

Handle to a graph.


### -param pGraphProperties [in]

Pointer to a <a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a> structure that specifies new values for   the graph properties  that an application can set.

An application can set only the following fields of <a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a>:<ul>
<li><b>pwzFriendlyName</b></li>
<li><b>cPresenceMax</b></li>
<li><b>pwzComment</b></li>
<li><b>ulPresenceLifetime</b></li>
</ul>
<div class="alert"><b>Note</b>   If remaining fields are set, then they are ignored.</div>
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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot access a peer  graph.

</td>
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
The handle to a peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



You can modify
the <b>pwzFriendlyName</b>,
<b>cPresenceMax</b>, <b>pwzComment</b>and
<b>ulPresenceLifetime</b> members of the <a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/f62fadf8-8cc2-4597-93b0-e076258ccd6a">PeerGraphGetProperties</a>
 

 

