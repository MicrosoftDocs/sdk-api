---
UID: NF:p2p.PeerGraphPeerTimeToUniversalTime
title: PeerGraphPeerTimeToUniversalTime function
author: windows-sdk-content
description: The PeerGraphPeerTimeToUniversalTime function converts the peer graph-maintained reference time value to a localized time value appropriate for display on the peer's computer.
old-location: p2p\peergraphpeertimetouniversaltime.htm
tech.root: P2PSdk
ms.assetid: 9cbb0b59-c116-4bd2-932f-2140595f4fad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerGraphPeerTimeToUniversalTime, PeerGraphPeerTimeToUniversalTime function [Peer Networking], p2p.peergraphpeertimetouniversaltime, p2p/PeerGraphPeerTimeToUniversalTime
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
 - PeerGraphPeerTimeToUniversalTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PeerGraphPeerTimeToUniversalTime
: 
---

# PeerGraphPeerTimeToUniversalTime function


## -description


The <b>PeerGraphPeerTimeToUniversalTime</b> function converts the peer graph-maintained reference time value to a localized time value appropriate for display on the peer's computer.


## -parameters




### -param hGraph [in]

Handle to the  peer graph this peer participates in. This handle is returned by the <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>, or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a> function.


### -param pftPeerTime [in]

Pointer to the peer time (UTC)  value, represented as a <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">FILETIME</a> structure.


### -param pftUniversalTime [out]

Pointer to the returned universal time value, represented as a <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">FILETIME</a> structure.


## -returns



Returns S_OK if the function succeeds; otherwise, the function returns one of the following values.

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
The handle to the graph is invalid.

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



<i>Universal time</i> is the UTC time derived from the peer's system clock.

<i>Peer time</i> is a common reference time maintained by the peer graph, expressed as Greenwich Mean Time.

Peer time should be  converted to universal time whenever it is necessary to display this value on the peer's computer, such as when displaying the creation time of a record. Likewise, time-sensitive actions, such as setting the expiration time for a record or searching for records based on modification time, should use time values converted from the computer-specific universal time to graph-specific peer time.

Universal time can be converted to peer time by calling the converse function <a href="https://msdn.microsoft.com/4d2c8943-cef5-4df3-96fe-447bd5bf37e8">PeerGraphUniversalTimeToPeerTime</a>.




## -see-also




<a href="https://msdn.microsoft.com/4d2c8943-cef5-4df3-96fe-447bd5bf37e8">PeerGraphUniversalTimeToPeerTime</a>
 

 

