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

# PeerPnrpResolve function


## -description


The <b>PeerPnrpResolve</b> function obtains the endpoint address(es) registered for a specific peer name.


## -parameters




### -param pcwzPeerName [in]

Pointer to a zero-terminated string that contains the peer name for which endpoint addresses will be obtained.


### -param pcwzCloudName [in, optional]

Pointer to a zero-terminated string that contains the name of the PNRP cloud under which to resolve the peer name. If <b>NULL</b>, the resolve is performed in all clouds. If PEER_PNRP_ALL_LINK_CLOUDS, the resolve is performed in all link local clouds. When "GLOBAL_", resolve will only take place in the global cloud.


### -param pcEndpoints [in, out]

The maximum number of endpoints to return in  <i>ppEndpoints</i>. Upon return, this parameter contains the actual number of endpoints in <i>ppEndpoints</i>.


### -param ppEndpoints [out]

Pointer to a list of <a href="https://msdn.microsoft.com/986e3bec-9915-4a7c-8f54-faf25fa2848c">PEER_PNRP_ENDPOINT_INFO</a> structures that contain the endpoints for which the peer name successfully resolved. Each endpoint contains one or more IP addresses at which the peer node can be reached.


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



This call is synchronous and will block until completed. For aysnchronous peer name resolution, call <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a> and obtain the resolved endpoint address when the supplied event is raised.

A handle must be resolved in a process separate of the process it was registered in. If a handle is registered and resolved within the same process it will not be recognized.

When  resolution is performed for all clouds, it is issued to each cloud simultaneously. The method will return as soon as it has received enough results from any combination of clouds.

The default resolve timeout used internally by this method is 30 seconds. If a  specific timeout is required,the asynchronous <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a> function should be used.




## -see-also




<a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>
 

 

