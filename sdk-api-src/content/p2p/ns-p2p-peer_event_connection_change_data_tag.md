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

# peer_event_connection_change_data_tag structure


## -description


  A <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> structure points to the <b>PEER_EVENT_CONNECTION_CHANGE_DATA</b> structure if one of the following peer events is triggered:
<ul>
<li><b>PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION</b></li>
<li><b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b></li>
<li><b>PEER_GROUP_EVENT_NEIGHBOR_CONNECTION</b></li>
<li><b>PEER_GROUP_EVENT_DIRECT_CONNECTION</b></li>
</ul>  The  <b>PEER_EVENT_CONNECTION_CHANGE_DATA</b> structure contains  updated information that includes changes to   a neighbor or direct connection.


## -struct-fields




### -field dwSize

Specifies the size of a structure.


### -field status

Specifies the type of change in a neighbor or direct connection. Valid values are the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_CONNECTED"></a><a id="peer_connected"></a><dl>
<dt><b><b>PEER_CONNECTED</b></b></dt>
</dl>
</td>
<td width="60%">
A new incoming or outgoing connection to the local node has been established.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_CONNECTION_FAILED"></a><a id="peer_connection_failed"></a><dl>
<dt><b><b>PEER_CONNECTION_FAILED</b></b></dt>
</dl>
</td>
<td width="60%">
An attempt to connect to a local node has failed. 

It is possible for a single attempt to connect to result in multiple connection failures. This will occur after the initial connection failure, when the peer infrastructure sets the <b>ullNextConnectionId</b> member to the Node ID and attempts a new connection.  If the <b>ullNextConnectionId</b> member is 0, no further connections will be attempted.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_DISCONNECTED"></a><a id="peer_disconnected"></a><dl>
<dt><b><b>PEER_DISCONNECTED</b></b></dt>
</dl>
</td>
<td width="60%">
An existing connection has been disconnected.

</td>
</tr>
</table>
 


### -field ullConnectionId

  Specifies the unique ID for a connection that has changed.


### -field ullNodeId

Specifies the unique ID for the node that has changed.


### -field ullNextConnectionId

 


### -field hrConnectionFailedReason

<b>Windows Vista or later.</b> Specifies the type of error when a connection fails.  <b>hrConnectionFailedReason</b> can return the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>PEER_E_CONNECTION_REFUSED</b></td>
<td>A connection has been established and refused. The remote node is already at  maximum number of connections or a connection already exists.</td>
</tr>
<tr>
<td><b>PEER_E_CONNECTION_FAILED</b></td>
<td>An attempt to connect to a remote node has failed.</td>
</tr>
<tr>
<td><b>PEER_E_CONNECTION_NOT_AUTHENTICATED </b></td>
<td>A connection is lost during the authentication phase. This is the result of a network failure or the  remote node breaking the connection.</td>
</tr>
</table>
 


#### - ullNextConnectionID

<b>Windows Vista or later.</b> Contains the next available node ID that the grouping or graphing APIs will attempt to connect to when a connection fails. If this member has a value of 0, no further connections will be attempted.


## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>
 

 

