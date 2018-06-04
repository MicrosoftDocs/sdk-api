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

# PeerPnrpUpdateRegistration function


## -description


The <b>PeerPnrpUpdateRegistration</b> function updates the PNRP registration information for a name.


## -parameters




### -param hRegistration [in]

Handle to a PNRP registration for the peer node obtained by a previous call to <a href="https://msdn.microsoft.com/18c26779-f50d-43bd-a772-763ceba25da8">PeerPnrpRegister</a>.


### -param pRegistrationInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/2825cb65-94b4-4bed-acff-7fa35a992284">PEER_PNRP_REGISTRATION_INFO</a> structure that contains the endpoint information for the registering peer node.


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



The <b>pwzCloudName</b>  and <b>cAddresses</b> members of the <a href="https://msdn.microsoft.com/2825cb65-94b4-4bed-acff-7fa35a992284">PEER_PNRP_REGISTRATION_INFO</a> provided in the <i>pRegistrationInfo</i> parameter cannot be changed with PeerPnrpUpdateRegistration. Attempting to do so will return an <b>E_INVALIDARG</b> error.

PeerPnrpUpdateRegistration has a maximum payload of 4k.




## -see-also




<a href="https://msdn.microsoft.com/18c26779-f50d-43bd-a772-763ceba25da8">PeerPnrpRegister</a>



<a href="https://msdn.microsoft.com/ac032cfb-b1d4-4fe0-8d27-7d378aaa6aff">PeerPnrpUnregister</a>
 

 

