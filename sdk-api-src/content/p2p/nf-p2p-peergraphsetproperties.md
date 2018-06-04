---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">
        PEER_GRAPH_PROPERTIES</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/f62fadf8-8cc2-4597-93b0-e076258ccd6a">PeerGraphGetProperties</a>
 

 

