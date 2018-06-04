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

# _PROJECTION_INFO2 structure


## -description


Used in the <a href="https://msdn.microsoft.com/b7cd637d-45ad-4e4c-b5b2-e85b142375ff">RAS_CONNECTION_4</a> structure as a placeholder for the <a href="https://msdn.microsoft.com/273af594-66f1-4d51-b597-3f09ee5c66cb">PPP_PROJECTION_INFO2</a> and <a href="https://msdn.microsoft.com/577a276e-e2f4-46d6-ae0b-2ba0f0bac67f">IKEV2_PROJECTION_INFO2</a> structures.


## -struct-fields




### -field projectionInfoType

A value that specifies if the projection is for a Point-to-Point (PPP) or an Internet Key Exchange version 2 (IKEv2) based tunnel. The following values are supported.

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
The data is a <a href="https://msdn.microsoft.com/273af594-66f1-4d51-b597-3f09ee5c66cb">PPP_PROJECTION_INFO2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_PROJECTION_INFO_TYPE"></a><a id="mprapi_ikev2_projection_info_type"></a><dl>
<dt><b>MPRAPI_IKEV2_PROJECTION_INFO_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The data is a <a href="https://msdn.microsoft.com/577a276e-e2f4-46d6-ae0b-2ba0f0bac67f">IKEV2_PROJECTION_INFO2</a> structure.

</td>
</tr>
</table>
 


### -field PppProjectionInfo

A <a href="https://msdn.microsoft.com/273af594-66f1-4d51-b597-3f09ee5c66cb">PPP_PROJECTION_INFO2</a> structure that is used for a PPP based tunnel.


### -field Ikev2ProjectionInfo

A <a href="https://msdn.microsoft.com/577a276e-e2f4-46d6-ae0b-2ba0f0bac67f">IKEV2_PROJECTION_INFO2</a> structure that is used for an IKEv2 based tunnel.

