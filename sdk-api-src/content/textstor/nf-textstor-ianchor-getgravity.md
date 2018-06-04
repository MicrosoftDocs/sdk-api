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

# IAnchor::GetGravity


## -description


The <b>IAnchor::GetGravity</b> method retrieves the gravity of the anchor in an <a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a> object.


## -parameters




### -param pgravity [out]

Pointer that receives a <a href="https://msdn.microsoft.com/12ec85b9-e65f-485d-8e42-164d2a988356">TsGravity</a> value that specifies the anchor gravity.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pgravity</i> pointer is invalid. 

</td>
</tr>
</table>
 




## -see-also




<a href="ranges.htm">Anchor Gravity</a>



<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/c532abcf-9ae0-4566-80f7-0bb4ae908fce">IAnchor::SetGravity</a>



<a href="https://msdn.microsoft.com/12ec85b9-e65f-485d-8e42-164d2a988356">TsGravity</a>
 

 

