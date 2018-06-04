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

# _PROJECTION_INFO structure


## -description


The <b>PROJECTION_INFO</b> structure  is used in the <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure as a placeholder for  the <a href="https://msdn.microsoft.com/f100a7d0-9f22-4cc6-8db0-684cff565e76">PPP_PROJECTION_INFO</a>  and <a href="https://msdn.microsoft.com/092ccaf9-d109-41a8-aa45-cf39f6bb70ca">IKEV2_PROJECTION_INFO</a> structures.


## -struct-fields




### -field projectionInfoType

A value that specifies if the projection is for a Point-to-Point (PPP) or an Internet Key Exchange version 2 (IKEv2) based tunnel. The following values are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_PPP_PROJECTION_INFO_TYPE"></a><a id="mprapi_ppp_projection_info_type"></a><dl>
<dt><b>MPRAPI_PPP_PROJECTION_INFO_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Data is a <a href="https://msdn.microsoft.com/f100a7d0-9f22-4cc6-8db0-684cff565e76">PPP_PROJECTION_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_PROJECTION_INFO_TYPE"></a><a id="mprapi_ikev2_projection_info_type"></a><dl>
<dt><b>MPRAPI_IKEV2_PROJECTION_INFO_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Data is a <a href="https://msdn.microsoft.com/092ccaf9-d109-41a8-aa45-cf39f6bb70ca">IKEV2_PROJECTION_INFO</a> structure.

</td>
</tr>
</table>
 


### -field PppProjectionInfo

A <a href="https://msdn.microsoft.com/f100a7d0-9f22-4cc6-8db0-684cff565e76">PPP_PROJECTION_INFO</a> structure that is used for a PPP based tunnel.


### -field Ikev2ProjectionInfo

A <a href="https://msdn.microsoft.com/092ccaf9-d109-41a8-aa45-cf39f6bb70ca">IKEV2_PROJECTION_INFO</a> structure that is used for an IKEv2 based tunnel.


## -see-also




<a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

