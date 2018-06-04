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

# PeerPnrpGetCloudInfo function


## -description


The <b>PeerPnrpCloudInfo</b> function retrieves information on the Peer Name Resolution Protocol (PNRP) clouds in which the calling peer is participating.


## -parameters




### -param pcNumClouds [out]

The number of PNRP clouds returned in <i>ppCloudInfo</i>.


### -param ppCloudInfo [out]

Pointer to a list of <a href="https://msdn.microsoft.com/b6121bae-22b7-4f23-ac8e-08822beef559">PEER_PNRP_CLOUD_INFO</a> structures that contain information about the PNRP clouds in which the calling peer is participating.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b6121bae-22b7-4f23-ac8e-08822beef559">PEER_PNRP_CLOUD_INFO</a>
 

 

