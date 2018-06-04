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

# PeerPnrpStartup function


## -description


The <b>PeerPnrpStartup</b> function starts the Peer Name Resolution Protocol (PNRP) service for the calling peer.


## -parameters




### -param wVersionRequested

The version of PNRP to use for this service instance. The default value is PNRP_VERSION (2).


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
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The provided version is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_SERVICE_NOT_AVAILABLE </b></dt>
</dl>
</td>
<td width="60%">
The Peer Collaboration infrastructure, which includes People Near Me, is not available. This code will also be returned whenever an attempt is made to utilize the Collaboration infrastructure from an elevated process.

</td>
</tr>
</table>
 




## -remarks



To shutdown the PNRP service for the calling peer and release all resources associated with it, call <a href="https://msdn.microsoft.com/e617fb5b-ace2-46b4-b165-4cd9cf891ac7">PeerPnrpShutdown</a>.




## -see-also




<a href="https://msdn.microsoft.com/e617fb5b-ace2-46b4-b165-4cd9cf891ac7">PeerPnrpShutdown</a>
 

 

