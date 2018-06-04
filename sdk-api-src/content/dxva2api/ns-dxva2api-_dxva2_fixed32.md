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

# _DXVA2_Fixed32 structure


## -description



Defines a 32-bit fixed-point number.




## -struct-fields




### -field Fraction

Fractional part of the number.


### -field Value

Integer part of the number.


### -field ll

Accesses the entire 32 bits of the number. You can use this member to compare <b>DXVA2_Fixed32</b> values.


## -remarks



To convert between floating-point numbers and <b>DXVA2_Fixed32</b> values, use the <a href="https://msdn.microsoft.com/f92c1d78-a2a7-469e-926a-7ba5ad8221e1">DXVA2FixedToFloat</a> and <a href="https://msdn.microsoft.com/2537e691-2137-4e4b-90a0-6749a6ceb144">DXVA2FloatToFixed</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

