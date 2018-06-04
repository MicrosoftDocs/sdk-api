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

# IMSVidClosedCaptioning::put_Enable


## -description


The <b>put_Enable</b> method enables or disables closed captioning.


## -parameters




### -param On [in]

Specifies whether to enable or disable the closed captioning feature. Use one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Enable closed captioning.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable closed captioning.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/070a208b-cf4c-41e1-9a5f-76cc444285c9">IMSVidClosedCaptioning Interface</a>



<a href="https://msdn.microsoft.com/2bb46aa7-fd94-4afa-9bba-769472e014ff">IMSVidClosedCaptioning::get_Enable</a>
 

 

