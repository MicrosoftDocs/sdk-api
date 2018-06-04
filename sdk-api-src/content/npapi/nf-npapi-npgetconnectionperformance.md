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

# NPGetConnectionPerformance function


## -description


Returns information about the expected performance of a connection used to access a network resource. The request can only be for a network resource that is currently connected.


## -parameters




### -param lpRemoteName [in]

Pointer to the local name or remote name for a connected resource.


### -param lpNetConnectInfo [out]

Pointer to a 
<a href="https://msdn.microsoft.com/0309667e-cb6c-406f-bb48-ed16602d38b2">NETCONNECTINFOSTRUCT</a> structure, which is filled in by the network provider if the provider has a connection to the network resource. All other fields of this structure, except the <b>cbStructure</b> field, are filled with zeros before the MPR passes the request on to the network providers. As a result, the provider has to write only to fields for which it has information available. Also, for rate values, a value of 1 means that the performance is better than can be represented in the unit.

The information returned may be an estimate. If the network cannot obtain information about the resource on the network, it can return information about the network adapter and its associated performance and then set the <b>dwFlags</b> field accordingly.


## -returns



If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
<i>lpRemoteName</i> is not a connected network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present.

</td>
</tr>
</table>
 



