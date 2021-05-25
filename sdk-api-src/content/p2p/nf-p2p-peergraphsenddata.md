---
UID: NF:p2p.PeerGraphSendData
title: PeerGraphSendData function (p2p.h)
description: The PeerGraphSendData function sends data to a neighbor node or a directly connected node.
helpviewer_keywords: ["PeerGraphSendData","PeerGraphSendData function [Peer Networking]","p2p.peergraphsenddata","p2p/PeerGraphSendData"]
old-location: p2p\peergraphsenddata.htm
tech.root: p2p
ms.assetid: 8ccb6f37-cb1b-41fd-a852-5a84cb5506f5
ms.date: 12/05/2018
ms.keywords: PeerGraphSendData, PeerGraphSendData function [Peer Networking], p2p.peergraphsenddata, p2p/PeerGraphSendData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGraphSendData
 - p2p/PeerGraphSendData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphSendData
---

# PeerGraphSendData function


## -description

The <b>PeerGraphSendData</b> function sends data to a  neighbor node  or a directly  connected node.

## -parameters

### -param hGraph [in]

Handle to the peer graph.

### -param ullConnectionId [in]

Specifies the unique ID of  the connection to send data on.

### -param pType [in]

Specifies an application-defined data type to send. 	This parameter cannot be <b>NULL</b>.

### -param cbData [in]

Specifies the number of bytes pointed to by <i>pvData</i>.

### -param pvData [in]

Pointer to the  data to send.

## -returns

Returns S_OK  if the operation succeeds; otherwise, the function returns one of the following values:

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
<dt><b>PEER_E_CONNECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No connection with the given ID exists.

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
The graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

The <b>PeerGraphSendData</b> function returns as soon as data has been sent to the network layer; the peer graphing layer does not wait for an acknowledgment from the other side of the connection.

<div class="alert"><b>Note</b>  In order to be able to receive data with a direct connection, an application must register for a peer event of type <b>PEER_GRAPH_EVENT_INCOMING_DATA</b>. See <a href="/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerGraphRegisterEvent</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopendirectconnection">PeerGraphOpenDirectConnection</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerGraphRegisterEvent</a>