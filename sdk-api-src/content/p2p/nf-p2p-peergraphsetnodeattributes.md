---
UID: NF:p2p.PeerGraphSetNodeAttributes
title: PeerGraphSetNodeAttributes function
author: windows-sdk-content
description: The PeerGraphSetNodeAttributes function sets the attributes of the PEER_NODE_INFO structure for the local node.
old-location: p2p\peergraphsetnodeattributes.htm
old-project: P2PSdk
ms.assetid: 334b6c88-4d5d-4e73-843f-2be07b9de9c9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerGraphSetNodeAttributes, PeerGraphSetNodeAttributes function [Peer Networking], p2p.peergraphsetnodeattributes, p2p/PeerGraphSetNodeAttributes
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
 - PeerGraphSetNodeAttributes
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: ADAM
---

# PeerGraphSetNodeAttributes function


## -description



      The <b>PeerGraphSetNodeAttributes</b> function sets the attributes of the <a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a> structure for the local node.


## -parameters




### -param hGraph [in]

Handle to the peer graph.


### -param pwzAttributes [in]

Pointer to  a string that represents the attributes the application associates with the local node. This string is a free-form text string that is specific to the application. Specify <b>NULL</b> to delete all attributes for the specified node.


## -returns



If the function call succeeds, the return value is S_OK. Otherwise, it  returns one of the following value.

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
 




## -remarks



To retrieve attributes for a node, call <a href="https://msdn.microsoft.com/7149aba3-d44b-4492-aa56-4d8dbfba7b7c">PeerGraphGetNodeInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a>



<a href="https://msdn.microsoft.com/7149aba3-d44b-4492-aa56-4d8dbfba7b7c">PeerGraphGetNodeInfo</a>
 

 

