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

# tagMAGTRANSFORM structure


## -description


Describes a transformation matrix that a magnifier control uses to magnify screen content.


## -struct-fields




### -field v

Type: <b>float[3]</b>

The transformation matrix.


## -remarks



The transformation matrix is 

 (<i>n</i>, 0.0, 0.0)

 (0.0, <i>n</i>, 0.0)

 (0.0, 0.0, 1.0) 

where <i>n</i> is the magnification factor.




## -see-also




<a href="https://msdn.microsoft.com/54fc86bc-283d-44ba-85ee-a0e370d3b64c">MagGetWindowTransform</a>



<a href="https://msdn.microsoft.com/2005f7de-5275-457e-a89f-794de5c66f5a">MagSetWindowTransform</a>



<b>Reference</b>
 

 

