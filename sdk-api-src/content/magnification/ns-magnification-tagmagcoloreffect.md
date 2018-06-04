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

# tagMAGCOLOREFFECT structure


## -description


Describes a color transformation matrix that a magnifier control uses to apply a color effect to magnified screen content.


## -struct-fields




### -field transform

 




#### - transform[5][5]

Type: <b>float</b>

The color transformation matrix.


## -remarks




The values in the matrix are for red, blue, green, alpha, and color translation. For more information, see 
<a href="https://msdn.microsoft.com/fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241">Using a Color Matrix to Transform a Single Color</a> in the Windows GDI+ documentation.
 





## -see-also




<a href="https://msdn.microsoft.com/d86d3e43-5da0-460c-b243-d0797f5d0911">MagGetColorEffect</a>



<a href="https://msdn.microsoft.com/53749109-5370-45e7-ba90-79ad1504c41e">MagSetColorEffect</a>



<b>Reference</b>
 

 

