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

# PeerPnrpRegister function


## -description


The <b>PeerPnrpRegister</b> function registers a peer with a PNRP cloud and returns a handle that can be used for registration updates.
<div class="alert"><b>Note</b>  When called, this function will block until the PNRP service has been initiated.</div><div> </div>

## -parameters




### -param pcwzPeerName [in]

Pointer to a zero-terminated Unicode string that contains the peer name to register with the PNRP service.


### -param pRegistrationInfo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/2825cb65-94b4-4bed-acff-7fa35a992284">PEER_PNRP_REGISTRATION_INFO</a> structure that contains the endpoint information for the registering peer node. If <b>NULL</b>, the API will register the peer with all known PNRP clouds, and any registered addresses are automatically selected by the infrastructure. 
  


### -param phRegistration [out]

Handle to the  PNRP registration for the calling peer node. Use this handle to update the registration or to deregister with the PNRP service.


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
<dt><b>PEER_E_IDENTITY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The local peer is using an identity that does not exist.

</td>
</tr>
</table>
 

Additionally, this function can return WSA values. For a complete list of possible values, see <a href="https://msdn.microsoft.com/adf40b1a-c5d6-418d-a012-cf6ba7d4fa24">PNRP NSP Error Codes</a>.




## -remarks



A  handle must be registered in a process separate of the process it will be resolved in. If a handle is registered and resolved within the same process it will not be recognized.

A name cannot be registered with an endpoint more than once. When updates to a registered name are required, use <a href="https://msdn.microsoft.com/628aa553-4a55-452b-bcca-4bb763fa6440">PeerPnrpUpdateRegistration</a>.

When <i>pRegistrationInfo</i> is <b>NULL</b>, or PEER_PNRP_AUTO_ADDRESSES is specified for <i>cAddresses</i>, the infrastructure will keep the addresses registered up to date as addresses change or cloud availability changes.




## -see-also




<a href="https://msdn.microsoft.com/ac032cfb-b1d4-4fe0-8d27-7d378aaa6aff">PeerPnrpUnregister</a>



<a href="https://msdn.microsoft.com/628aa553-4a55-452b-bcca-4bb763fa6440">PeerPnrpUpdateRegistration</a>
 

 

