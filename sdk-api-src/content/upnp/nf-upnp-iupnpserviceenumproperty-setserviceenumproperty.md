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

# IUPnPServiceEnumProperty::SetServiceEnumProperty


## -description


The <b>SetServiceEnumProperty</b> method is used to indicate opt-in to the delayed Service Control Protocol Description (SCPD) download and event subscription for the <a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> objects enumerated from the <a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a> object.


## -parameters




### -param dwMask






#### - dwMASK

Specifies a bit-wise flag to indicate an opt-in to the delayed SCPD download and even subscription. Possible values include:

<table>
<tr>
<th>Flag</th>
<th>Value</th>
</tr>
<tr>
<td>UPNP_SERVICE_DELAY_SCPD_AND_SUBSCRIPTION</td>
<td>0x1</td>
</tr>
</table>
 


## -returns



Returns <b>S_OK</b> on success. Otherwise, this method returns <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/B63CCE08-548F-44D3-BAE3-84E4358F25AD">IUPnPServiceEnumProperty</a>
 

 

