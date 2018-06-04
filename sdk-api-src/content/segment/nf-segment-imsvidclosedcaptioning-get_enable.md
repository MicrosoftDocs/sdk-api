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

# IMSVidClosedCaptioning::get_Enable


## -description


The <b>get_Enable</b> method queries whether closed captioning is enabled.


## -parameters




### -param On






#### - pOn [out]

Pointer to a variable that receives one of the following values.

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
<td>Closed captioning is enabled.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Closed captioning is disabled.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/070a208b-cf4c-41e1-9a5f-76cc444285c9">IMSVidClosedCaptioning Interface</a>



<a href="https://msdn.microsoft.com/2485b634-24e9-4945-ae46-0ca7fdb9d92b">IMSVidClosedCaptioning::put_Enable</a>
 

 

