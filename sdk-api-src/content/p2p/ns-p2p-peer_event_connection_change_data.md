---
UID: NS:p2p.peer_event_connection_change_data_tag
title: PEER_EVENT_CONNECTION_CHANGE_DATA (p2p.h)
description: Points to the PEER_EVENT_CONNECTION_CHANGE_DATA structure if one of the following peer events is triggered.
helpviewer_keywords: ["*PPEER_EVENT_CONNECTION_CHANGE_DATA","PEER_CONNECTED","PEER_CONNECTION_FAILED","PEER_DISCONNECTED","PEER_EVENT_CONNECTION_CHANGE_DATA","PEER_EVENT_CONNECTION_CHANGE_DATA structure [Peer Networking]","PPEER_EVENT_CONNECTION_CHANGE_DATA","PPEER_EVENT_CONNECTION_CHANGE_DATA structure pointer [Peer Networking]","p2p.peer_event_connection_change_data","p2p/PPEER_EVENT_CONNECTION_CHANGE_DATA","p2p/peer_event_connection_change_data_tag"]
old-location: p2p\peer_event_connection_change_data.htm
tech.root: p2p
ms.assetid: 0d73432c-c1e5-4fa9-a812-377b22a47440
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_CONNECTION_CHANGE_DATA, PEER_CONNECTED, PEER_CONNECTION_FAILED, PEER_DISCONNECTED, PEER_EVENT_CONNECTION_CHANGE_DATA, PEER_EVENT_CONNECTION_CHANGE_DATA structure [Peer Networking], PPEER_EVENT_CONNECTION_CHANGE_DATA, PPEER_EVENT_CONNECTION_CHANGE_DATA structure pointer [Peer Networking], p2p.peer_event_connection_change_data, p2p/PPEER_EVENT_CONNECTION_CHANGE_DATA, p2p/peer_event_connection_change_data_tag'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_EVENT_CONNECTION_CHANGE_DATA, *PPEER_EVENT_CONNECTION_CHANGE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_connection_change_data_tag
 - p2p/peer_event_connection_change_data_tag
 - PPEER_EVENT_CONNECTION_CHANGE_DATA
 - p2p/PPEER_EVENT_CONNECTION_CHANGE_DATA
 - PEER_EVENT_CONNECTION_CHANGE_DATA
 - p2p/PEER_EVENT_CONNECTION_CHANGE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_EVENT_CONNECTION_CHANGE_DATA
---

# PEER_EVENT_CONNECTION_CHANGE_DATA structure


## -description

  A <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a> structure points to the <b>PEER_EVENT_CONNECTION_CHANGE_DATA</b> structure if one of the following peer events is triggered:
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
<dt><b>PEER_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
A new incoming or outgoing connection to the local node has been established.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_CONNECTION_FAILED"></a><a id="peer_connection_failed"></a><dl>
<dt><b>PEER_CONNECTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An attempt to connect to a local node has failed. 

It is possible for a single attempt to connect to result in multiple connection failures. This will occur after the initial connection failure, when the peer infrastructure sets the <b>ullNextConnectionId</b> member to the Node ID and attempts a new connection.  If the <b>ullNextConnectionId</b> member is 0, no further connections will be attempted.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_DISCONNECTED"></a><a id="peer_disconnected"></a><dl>
<dt><b>PEER_DISCONNECTED</b></dt>
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

<b>Windows Vista or later.</b> Contains the next available node ID that the grouping or graphing APIs will attempt to connect to when a connection fails. If this member has a value of 0, no further connections will be attempted.

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



## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a>



[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)