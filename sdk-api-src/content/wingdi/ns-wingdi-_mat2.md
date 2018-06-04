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

# _MAT2 structure


## -description



The <b>MAT2</b> structure contains the values for a transformation matrix used by the <a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a> function.




## -struct-fields




### -field eM11

A fixed-point value for the M11 component of a 3 by 3 transformation matrix.


### -field eM12

A fixed-point value for the M12 component of a 3 by 3 transformation matrix.


### -field eM21

A fixed-point value for the M21 component of a 3 by 3 transformation matrix.


### -field eM22

A fixed-point value for the M22 component of a 3 by 3 transformation matrix.


## -remarks



The identity matrix produces a transformation in which the transformed graphical object is identical to the source object. In the identity matrix, the value of <b>eM11</b> is 1, the value of <b>eM12</b> is zero, the value of <b>eM21</b> is zero, and the value of <b>eM22</b> is 1.




## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a>
 

 

