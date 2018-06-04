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

# ITToneDetectionEvent::get_AppSpecific


## -description


The 
<b>get_AppSpecific</b> method gets the application-defined tag that identifies the tone associated with the tone detection event.


## -parameters




### -param plAppSpecific [out]

Pointer to a value to receive the application-specific identifier for the tone, as defined in the 
<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a> object or in the 
<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a> structure.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plAppSpecific</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1e0f71a2-1aae-46b7-9147-7bf9da4d9503">ITToneDetectionEvent</a>



<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a>
 

 

