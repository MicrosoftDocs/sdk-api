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

# PeerGraphOpenDirectConnection function


## -description



      The <b>PeerGraphOpenDirectConnection</b> function allows an application to establish a direct connection with a node in a peer graph. The connection can only be made if the node to which  the application is connecting has subscribed to the <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> event. The application can then   send data directly to another node.  A call to this function is asynchronous.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param pwzPeerId [in]

Pointer to  the unique ID of a user or node to connect to. This parameter is used to identify a specific user because multiple identities can be attached to the specified address.


### -param pAddress [in]

Pointer to a <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structure that contains the address of the node to  connect to.


### -param pullConnectionId [out]

Receives the connection ID for the requested connection.


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
The graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>—before using this function.

</td>
</tr>
</table>
 




## -remarks



A call to <b>PeerGraphOpenDirectConnection</b> is an asynchronous call.  A <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> event is triggered to inform the application of the direct connection's success or failure. The actual status of the function's success or failure is given in the <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">
        PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/e5547292-7f6f-456c-b47a-5d5948f51a7f">PeerGraphCloseDirectConnection</a>



<a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>
 

 

