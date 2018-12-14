---
UID: NF:p2p.PeerPnrpGetEndpoint
title: PeerPnrpGetEndpoint function
author: windows-sdk-content
description: Retrieves a peer endpoint address resolved during an asynchronous peer name resolution operation.
old-location: p2p\peerpnrpgetendpoint.htm
tech.root: P2PSdk
ms.assetid: d81b0aab-90b5-4583-b554-efe38c220e59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerPnrpGetEndpoint, PeerPnrpGetEndpoint function [Peer Networking], p2p.peerpnrpgetendpoint, p2p/PeerPnrpGetEndpoint
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
 - PeerPnrpGetEndpoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerPnrpGetEndpoint function


## -description


The <b>PeerPnrpGetEndpoint</b> function retrieves a peer endpoint address resolved during an asynchronous peer name resolution operation.


## -parameters




### -param hResolve [in]

The handle to the asynchronous peer name resolution operation returned by a previous call to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>.


### -param ppEndpoint [out]

Pointer to the address of a <a href="https://msdn.microsoft.com/986e3bec-9915-4a7c-8f54-faf25fa2848c">PEER_PNRP_ENDPOINT_INFO</a> structure that contains an endpoint address for the peer name supplied in the previous call to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>.

This data returned by this parameter must be freed by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
All endpoint addresses have been retrieved for the peer.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a> creates a handle to an asynchronous peer name resolution operation. 

Whenever an endpoint is found, the event handle provided in <i>hEvent</i> is signaled, and <b>PeerPnrpGetEndpoint</b> must be called with the <i>phResolve</i> handle by the application to obtain that endpoint.

The last event specifies the PEER_E_NO_MORE error code, indicating that all endpoints corresponding to the peer name supplied to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a> have been found. At this time, the application must close the handle with a call to <a href="https://msdn.microsoft.com/b700a195-57c4-481a-93d2-82d543f5c6c6">PeerPnrpEndResolve</a>.




## -see-also




<a href="https://msdn.microsoft.com/b700a195-57c4-481a-93d2-82d543f5c6c6">PeerPnrpEndResolve</a>



<a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>
 

 

