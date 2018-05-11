---
UID: NS:mprapi._PROJECTION_INFO
title: "_PROJECTION_INFO"
author: windows-driver-content
description: Is used in the RAS_CONNECTION_EX structure as a placeholder for the PPP_PROJECTION_INFO and IKEV2_PROJECTION_INFO structures.
old-location: rras\projection_info.htm
old-project: RRAS
ms.assetid: 3f87d09a-2408-4fe4-97f9-61ed9b5d2fa5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PPROJECTION_INFO, MPRAPI_IKEV2_PROJECTION_INFO_TYPE, MPRAPI_PPP_PROJECTION_INFO_TYPE, PPROJECTION_INFO, PPROJECTION_INFO structure pointer [RAS], PROJECTION_INFO, PROJECTION_INFO structure [RAS], _PROJECTION_INFO, mprapi/PPROJECTION_INFO, mprapi/PROJECTION_INFO, rras.projection_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROJECTION_INFO, *PPROJECTION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	PROJECTION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

