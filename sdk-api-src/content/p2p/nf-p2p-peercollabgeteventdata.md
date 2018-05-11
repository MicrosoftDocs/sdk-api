---
UID: NF:p2p.PeerCollabGetEventData
title: PeerCollabGetEventData function
author: windows-driver-content
description: Obtains the data associated with a peer collaboration event raised on the peer.
old-location: p2p\peercollabgeteventdata.htm
old-project: P2PSdk
ms.assetid: ee410a47-91a6-48ed-8c05-128a141a5c98
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerCollabGetEventData, PeerCollabGetEventData function [Peer Networking], p2p.peercollabgeteventdata, p2p/PeerCollabGetEventData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	P2P.dll
api_name:
-	PeerCollabGetEventData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerCollabGetEventData function


## -description


The <b>PeerCollabGetEventData</b> function obtains the data associated with a peer collaboration event raised on the peer.


## -parameters




### -param hPeerEvent [in]

The peer collaboration network event handle obtained by a call to <a href="https://msdn.microsoft.com/db7daf08-8d79-493f-8df5-172dae498df0">PeerCollabRegisterEvent</a>.


### -param ppEventData [out]

Pointer to a list of <a href="https://msdn.microsoft.com/4ddf200d-0b7a-4e99-b7db-19b4e0412711">PEER_COLLAB_EVENT_DATA</a> structures that contain data about the peer collaboration network event. These data structures must be freed after use by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

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
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_S_NO_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The  event data is not present.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

