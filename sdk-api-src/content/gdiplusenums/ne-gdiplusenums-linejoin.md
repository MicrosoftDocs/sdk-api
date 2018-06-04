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

# LineJoin enumeration


## -description


The <b>LineJoin</b> enumeration specifies how to join two lines that are drawn by the same pen and whose ends meet. At the intersection of the two line ends, a line join makes the join look more continuous. 


## -enum-fields




### -field LineJoinMiter

Specifies a mitered join. This produces a sharp corner or a clipped corner, depending on whether the length of the miter exceeds the miter limit. 


### -field LineJoinBevel

Specifies a beveled join. This produces a diagonal corner. 


### -field LineJoinRound

Specifies a circular join. This produces a smooth, circular arc between the lines. 


### -field LineJoinMiterClipped

Specifies a mitered join. This produces a sharp corner or a beveled corner, depending on whether the length of the miter exceeds the miter limit. 


## -remarks



The miter length is the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls outside of the join. The miter length can be large when the angle between two lines is small. The miter limit is the maximum allowed ratio of miter length to stroke width. The default value is 10.0f.

When using <b><b>LineJoinMiter</b></b> and the actual ratio exceeds the miter limit, the corner is clipped perpendicular to the miter at a distance from the inner corner that is the product of the miter limit and the pen width. 

<img alt="Illustration showing two lines with a corner that is clipped: the outside walls of the lines do not meet at a point" src="images/linejoinmiter.png"/>
When using <b><b>LineJoinMiterClipped</b></b> and the miter limit is exceeded, the join is drawn as if its type were <b><b>LineJoinBevel</b></b>; that is, when the line walls on the inside of the join meet, then a joining line is drawn between the line walls on the outside of the join.

<img alt="Illustration showing two lines with a corner that is beveled" src="images/linejoinbevel.png"/>



## -see-also




<a href="https://msdn.microsoft.com/277824b0-fa76-4b7b-97a0-c2be79a4b06f">Pen::SetLineJoin</a>



<a href="https://msdn.microsoft.com/2fd2ac24-40e6-49a6-a514-1233e2075f45">Pen::SetMiterLimit</a>
 

 

