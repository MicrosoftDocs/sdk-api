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

# DrvCopyBits function


## -description


The <b>DrvCopyBits</b> function translates between device-managed raster surfaces and GDI standard-format bitmaps. 


## -parameters




### -param psoDest

Pointer to the destination <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure for the copy operation.


### -param psoSrc

Pointer to the source SURFOBJ structure for the copy operation.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that defines a clip region on the destination surface.


### -param pxlo

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a> structure that defines the translation of color indices between the source and target surfaces. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.


### -param prclDest

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines the area to be modified. This structure uses the coordinate system of the destination surface. The lower and right edges of this rectangle are not part of the bit-block transfer, meaning the rectangle is lower right exclusive.

<b>DrvCopyBits</b> is never called with an empty destination rectangle. The two points that define the rectangle are always well-ordered.


### -param pptlSrc

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the upper-left corner of the source rectangle.


## -returns



The return value is <b>TRUE</b> if the source surface is successfully copied to the destination surface.




## -remarks



The driver may optionally hook <b>DrvCopyBits</b>. If so, GDI will call <b>DrvCopyBits</b> when it needs to copy from one surface to another and at least one of the surfaces is device-managed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a>
 

 

