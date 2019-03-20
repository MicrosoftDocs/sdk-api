---
UID: NF:p2p.PeerGraphCreate
title: PeerGraphCreate function (p2p.h)
author: windows-sdk-content
description: The PeerGraphCreate function creates a new peer graph. An application can specify information about a peer graph, and the type of security that a peer graph uses. A handle to a peer graph is returned, but a network connection is not established.
old-location: p2p\peergraphcreate.htm
tech.root: P2PSdk
ms.assetid: 62e3ec57-378c-4322-9ad4-a40d98e03dab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerGraphCreate, PeerGraphCreate function [Peer Networking], p2p.peergraphcreate, p2p/PeerGraphCreate
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
 - PeerGraphCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphCreate function


## -description


The <b>PeerGraphCreate</b> function creates a  new peer graph.  An application can  specify information about a peer graph, and the type of security that a  peer graph uses. A handle to a peer graph is returned, but a network connection is not established.


## -parameters




### -param pGraphProperties [in]

All of the properties of a peer graph in the <a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a> structure.


### -param pwzDatabaseName [in]

The name of a record database to associate with a peer graph when it is created. The record database name must be a valid file name. Do not include a path with the file name.  For a complete list of rules regarding file names, see  the Naming a File item in the list of  <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">Graphing Reference_Links</a>.


### -param pSecurityInterface [in]

The information about a security provider for a peer graph in the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a> structure.


### -param phGraph [out]

Receives a handle to the peer graph that is created. When this handle is not required anymore, free it by calling <a href="https://msdn.microsoft.com/7600da14-7641-4b5c-b5ba-e33ffc28097c">PeerGraphClose</a>.


## -returns



Returns <b>S_OK</b> if the operation succeeds. Otherwise, the function returns one of the following values.

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
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_DUPLICATE_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
A database with a specified peer graph ID that already exists.

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
 




## -remarks



If you develop your own Security Service Provider (SSP), your application must not call the Peer Graphing API to access data in the peer graphing database, because that can cause a deadlock situation.  Instead, the application must use a cached copy of the information. The cached copy is not created by the Peer Graphing API. The application must provide a mechanism for caching this data.

After   <b>PeerGraphCreate</b> is called, the  application can subscribe to events before it calls <a href="https://msdn.microsoft.com/bac893d4-8f4d-4e1f-953b-1b289c5f18be">PeerGraphListen</a>.




## -see-also




<a href="https://msdn.microsoft.com/15b4eeb4-1040-4f07-8e79-2c09aab9f926">PEER_GRAPH_PROPERTIES</a>



<a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a>



<a href="https://msdn.microsoft.com/7600da14-7641-4b5c-b5ba-e33ffc28097c">PeerGraphClose</a>



<a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a>



<a href="https://msdn.microsoft.com/bac893d4-8f4d-4e1f-953b-1b289c5f18be">PeerGraphListen</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>
 

 

