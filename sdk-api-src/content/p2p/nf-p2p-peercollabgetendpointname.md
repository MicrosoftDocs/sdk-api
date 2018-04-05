---
UID: NF:p2p.PeerCollabGetEndpointName
title: PeerCollabGetEndpointName function
author: windows-driver-content
description: Retrieves the name of the current endpoint of the calling peer, as previously set by a call to PeerCollabSetEndpointName.
old-location: p2p\peercollabgetendpointname.htm
old-project: P2PSdk
ms.assetid: f6165772-be55-4b56-bc70-dfa2c4a40c61
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PeerCollabGetEndpointName, PeerCollabGetEndpointName function [Peer Networking], p2p.peercollabgetendpointname, p2p/PeerCollabGetEndpointName
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
-	PeerCollabGetEndpointName
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PeerCollabGetEndpointName function


## -description


The <b>PeerCollabGetEndpointName</b> function retrieves the name of the current endpoint of the calling peer, as previously set by a call to <a href="https://msdn.microsoft.com/9b8d0559-c70e-4b05-bd73-1eb3b2e8f9c8">PeerCollabSetEndpointName</a>.


## -parameters




### -param ppwzEndpointName [out]

Pointer to a zero-terminated Unicode string name of the peer endpoint currently used by the calling application.


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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The operation requires the user to be signed in.

</td>
</tr>
</table>
 




## -remarks



The endpoint name is limited to 25 Unicode characters. To free this data call <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/9b8d0559-c70e-4b05-bd73-1eb3b2e8f9c8">PeerCollabSetEndpointName</a>
 

 

