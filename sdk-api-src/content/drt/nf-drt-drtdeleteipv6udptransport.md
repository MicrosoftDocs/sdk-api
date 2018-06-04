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

# DrtDeleteIpv6UdpTransport function


## -description


The <b>DrtDeleteIpv6UdpTransport</b> function deletes a  transport based on the IPv6 UDP protocol.


## -parameters




### -param hTransport [in]

The DRT transport handle specifying the transport to delete.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
<i>hTransport</i> is <b>NULL</b> or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_EXECUTING_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The transport provider is currently executing a method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_STILL_BOUND</b></dt>
</dl>
</td>
<td width="60%">
The transport is still bound.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORTPROVIDER_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
All clients have not called <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the transport.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also surface errors returned by underlying calls to <a href="https://msdn.microsoft.com/27d8d6ab-679d-4b7b-bf90-7b0859e7e048">PeerPnrpStartup</a> or <a href="https://msdn.microsoft.com/27a1b563-7bbe-4117-8bc3-19dd47360308">PeerIdentityGetCryptKey</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/def3120b-98b6-4e31-8166-822cea7fea69">DrtCreateIpv6UdpTransport</a>
 

 

