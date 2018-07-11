---
UID: NF:p2p.PeerGraphGetEventData
title: PeerGraphGetEventData function
author: windows-sdk-content
description: The PeerGraphGetEventData function retrieves peer events. An application calls this function until the return value PEER_S_NO_EVENT_DATA is returned, which indicates that a call is successful, but that there are no more peer events to retrieve.
old-location: p2p\peergraphgeteventdata.htm
old-project: p2psdk
ms.assetid: b64bb920-3fbc-4927-a1b1-39c99850bdd5
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PeerGraphGetEventData, PeerGraphGetEventData function [Peer Networking], p2p.peergraphgeteventdata, p2p/PeerGraphGetEventData
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphGetEventData
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: ADAM
---

# PeerGraphGetEventData function


## -description



      The <b>PeerGraphGetEventData</b> function retrieves peer events. An application  calls this function until the  return value   <b>PEER_S_NO_EVENT_DATA</b> is returned, which indicates that a call is successful, but that there are no more peer events to retrieve.


## -parameters




### -param hPeerEvent [in]

Peer event handle obtained by a call to <a href="https://msdn.microsoft.com/3ed963ba-0b9d-4de8-a610-b07cf49ed27f">PeerGraphRegisterEvent</a>.


### -param ppEventData [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> structure that contains the data about an event notification.   When this structure is not needed, free it by calling <a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a>.


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
One parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_S_NO_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The function call succeeds, but there is no data associated with a peer event.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A peer graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



Peer event data is returned in  a <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> structure.  The type of data structure that <b>PEER_GRAPH_EVENT_DATA</b> points to depends  on which event is triggered.




## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">
        PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a>



<a href="https://msdn.microsoft.com/3ed963ba-0b9d-4de8-a610-b07cf49ed27f">PeerGraphRegisterEvent</a>



<a href="https://msdn.microsoft.com/de37bb9a-e1b2-4448-9610-566f77acf542">PeerGraphUnregisterEvent</a>
 

 

