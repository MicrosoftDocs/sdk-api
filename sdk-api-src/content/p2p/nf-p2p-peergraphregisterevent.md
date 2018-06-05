---
UID: NF:p2p.PeerGraphRegisterEvent
title: PeerGraphRegisterEvent function
author: windows-sdk-content
description: The PeerGraphRegisterEvent function registers a peer's request to be notified of changes associated with a peer graph and event type.
old-location: p2p\peergraphregisterevent.htm
old-project: P2PSdk
ms.assetid: 3ed963ba-0b9d-4de8-a610-b07cf49ed27f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerGraphRegisterEvent, PeerGraphRegisterEvent function [Peer Networking], p2p.peergraphregisterevent, p2p/PeerGraphRegisterEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2PGraph.dll
api_name:
-	PeerGraphRegisterEvent
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphRegisterEvent function


## -description



      The <b>PeerGraphRegisterEvent</b> function registers a peer's request to be  notified of changes associated with a peer graph and event type.


## -parameters




### -param hGraph [in]

Handle to the peer graph.


### -param hEvent [in]

Handle created by <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">CreateEvent</a> that the application is signaled on  when an event is triggered.  When an application is signaled, it must call <a href="https://msdn.microsoft.com/b64bb920-3fbc-4927-a1b1-39c99850bdd5">PeerGraphGetEventData</a> to retrieve events until PEER_S_NO_EVENT_DATA returned.


### -param cEventRegistrations [in]

Specifies the number of <a href="https://msdn.microsoft.com/6725eba9-af61-4088-96e0-d0bf943902ea">
        PEER_GRAPH_EVENT_REGISTRATION</a> structures in <i>pEventRegistrations</i>.


### -param pEventRegistrations [in]

Points to an array of <a href="https://msdn.microsoft.com/6725eba9-af61-4088-96e0-d0bf943902ea">
        PEER_GRAPH_EVENT_REGISTRATION</a> structures that specify what events the application requests notifications for.


### -param phPeerEvent [out]

Receives a <b>HPEEREVENT</b> handle. This handle must be used when calling <a href="https://msdn.microsoft.com/de37bb9a-e1b2-4448-9610-566f77acf542">PeerGraphUnregisterEvent</a> to stop receiving  notifications.


## -returns



If the function call succeeds, the return value is S_OK. Otherwise, it  returns one of the following values.

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
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid.

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
 




## -see-also




<a href="https://msdn.microsoft.com/6725eba9-af61-4088-96e0-d0bf943902ea">
        PEER_GRAPH_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/b64bb920-3fbc-4927-a1b1-39c99850bdd5">PeerGraphGetEventData</a>



<a href="https://msdn.microsoft.com/de37bb9a-e1b2-4448-9610-566f77acf542">PeerGraphUnregisterEvent</a>
 

 

