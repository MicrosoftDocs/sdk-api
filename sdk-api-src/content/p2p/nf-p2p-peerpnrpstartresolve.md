---
UID: NF:p2p.PeerPnrpStartResolve
title: PeerPnrpStartResolve function
author: windows-sdk-content
description: Starts an asynchronous peer name resolution operation.
old-location: p2p\peerpnrpstartresolve.htm
tech.root: P2PSdk
ms.assetid: 140ecca5-85fe-480e-bc69-86e0bc69ad2e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerPnrpStartResolve, PeerPnrpStartResolve function [Peer Networking], p2p.peerpnrpstartresolve, p2p/PeerPnrpStartResolve
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerPnrpStartResolve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerPnrpStartResolve function


## -description


The <b>PeerPnrpStartResolve</b> function starts an asynchronous peer name resolution operation.


## -parameters




### -param pcwzPeerName [in]

Pointer to a zero-terminated string that contains the peer name for which endpoint addresses will be obtained.


### -param pcwzCloudName [in, optional]

Pointer to a zero-terminated string that contains the name of the PNRP cloud under which to resolve the peer name. If <b>NULL</b>, resolution is performed for all clouds. If PEER_PNRP_ALL_LINK_CLOUDS, resolution is performed for all link local clouds. When "GLOBAL_" is specified, resolution takes place in the global cloud.


### -param cMaxEndpoints [in, optional]

The maximum number of endpoints to return for the peer name.


### -param hEvent [in]

Handle to the event signaled when a peer endpoint is resolved for the supplied peer name and are ready for consumption by calling PeerPnrpGetEndpoint. This event is signaled for every endpoint discovered by the PNRP service. If PEER_NO_MORE is returned by a call to <a href="https://msdn.microsoft.com/d81b0aab-90b5-4583-b554-efe38c220e59">PeerPnrpGetEndpoint</a>, then all endpoints have been found for that peer.


### -param phResolve [out]

Handle to this peer name resolution request. This handle must be provided to <a href="https://msdn.microsoft.com/b700a195-57c4-481a-93d2-82d543f5c6c6">PeerPnrpEndResolve</a> after the resolution events are raised and the endpoints are obtained with corresponding calls to <a href="https://msdn.microsoft.com/d81b0aab-90b5-4583-b554-efe38c220e59">PeerPnrpGetEndpoint</a>, or if the operation fails.


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
</table>
 




## -remarks



<b>PeerPnrpStartResolve</b> creates a handle to an asynchronous peer name resolution operation. 

Whenever an endpoint is found, the event handle provided in <i>hEvent</i> is signaled, and <a href="https://msdn.microsoft.com/d81b0aab-90b5-4583-b554-efe38c220e59">PeerPnrpGetEndpoint</a> must be called with the <i>phResolve</i> handle by the application to obtain that endpoint.

The last event specifies the PEER_E_NO_MORE error code, indicating that all endpoints corresponding to the peer name supplied to <b>PeerPnrpStartResolve</b> have been found. At this time, the application must close the handle with a call to <a href="https://msdn.microsoft.com/b700a195-57c4-481a-93d2-82d543f5c6c6">PeerPnrpEndResolve</a>.

A handle must be resolved in a process separate from the process in which it was registered. If a handle is registered and resolved within the same process it will not be recognized.




## -see-also




<a href="https://msdn.microsoft.com/b700a195-57c4-481a-93d2-82d543f5c6c6">PeerPnrpEndResolve</a>



<a href="https://msdn.microsoft.com/d81b0aab-90b5-4583-b554-efe38c220e59">PeerPnrpGetEndpoint</a>



<a href="https://msdn.microsoft.com/dd66ab38-bb3e-46f5-943a-bcdae90acae0">PeerPnrpResolve</a>
 

 

