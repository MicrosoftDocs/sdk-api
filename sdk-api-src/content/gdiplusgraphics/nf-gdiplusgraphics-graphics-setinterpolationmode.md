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

# Graphics::SetInterpolationMode


## -description


The <b>Graphics::SetInterpolationMode</b> method sets the interpolation mode of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.


## -parameters




### -param interpolationMode [in]

Type: <b><a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a></b>

Element of the <a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a> enumeration that specifies the interpolation mode. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/a9f3b27c-cb16-4d52-9970-ea3708bd1e0c">Graphics::GetInterpolationMode</a>



<a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a>



<a href="https://msdn.microsoft.com/3aeead47-78da-4ab3-9126-2fbe9e341e48">Using Interpolation Mode to Control Image Quality During Scaling</a>
 

 

