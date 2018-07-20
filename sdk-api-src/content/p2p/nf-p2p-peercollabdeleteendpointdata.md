---
UID: NF:p2p.PeerCollabDeleteEndpointData
title: PeerCollabDeleteEndpointData function
author: windows-sdk-content
description: Deletes the peer endpoint data on the calling peer node that matches the supplied endpoint data.
old-location: p2p\peercollabdeleteendpointdata.htm
old-project: p2psdk
ms.assetid: bafaef04-d7f6-4873-bd38-db156817b0c8
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: PeerCollabDeleteEndpointData, PeerCollabDeleteEndpointData function [Peer Networking], p2p.peercollabdeleteendpointdata, p2p/PeerCollabDeleteEndpointData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabDeleteEndpointData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabDeleteEndpointData function


## -description


The <b>PeerCollabDeleteEndpointData</b> function deletes the peer endpoint data on the calling peer node that matches the supplied endpoint data.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint information to delete from the current peer node.


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
</table>
 




## -remarks



The function <b>PeerCollabDeleteEndpointData</b> is used to remove cached endpoint data previously retrieved by  <a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a> when it is no longer required. Any data obtained through <b>PeerCollabRefreshEndpointData</b> remains in memory until <b>PeerCollabDeleteEndpointData</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a>
 

 

