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

# IInkDrawingAttributes::put_RasterOperation


## -description



Gets or sets a value that defines how the colors of the pen and background interact.



This property is read/write.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/34403724-b883-4c03-8784-fe8f205d3da6">InkRasterOperation</a> enumeration defines values for performing raster operations on drawn ink. For example, if you want to perform subtractive transparency, set the raster value to MaskPen.

For a complete list of available raster operations, see the <a href="https://msdn.microsoft.com/34403724-b883-4c03-8784-fe8f205d3da6">InkRasterOperation</a> enumeration type.

<div class="alert"><b>Note</b>  Many printers do not support many of the available raster operations. Because of this, the colors displayed may be different than the colors printed. This is directly related to the printer drivers or printer hardware. You may have to experiment to determine which printers can produce the correct output when various raster operations are set on ink.</div>
<div> </div>
When the <b>RasterOperation</b> property is set to anything other than <a href="https://msdn.microsoft.com/34403724-b883-4c03-8784-fe8f205d3da6">InkRasterOperation.IRO_CopyPen</a>, all drawing attributes-anti-aliasing, smoothing, transparency, and pressure-are ignored.




## -see-also




<a href="tablet.iinkdrawingattributes">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/34403724-b883-4c03-8784-fe8f205d3da6">InkRasterOperation Enumeration</a>
 

 

