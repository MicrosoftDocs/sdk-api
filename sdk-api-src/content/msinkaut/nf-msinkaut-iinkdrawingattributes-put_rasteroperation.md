---
UID: NF:msinkaut.IInkDrawingAttributes.put_RasterOperation
title: IInkDrawingAttributes::put_RasterOperation
author: windows-sdk-content
description: Gets or sets a value that defines how the colors of the pen and background interact.
old-location: tablet\inkdrawingattributes_rasteroperation.htm
old-project: tablet
ms.assetid: 8e3681a7-c5be-4104-b740-9f23d141f6cb
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 8e3681a7-c5be-4104-b740-9f23d141f6cb, IInkDrawingAttributes interface [Tablet PC],RasterOperation property, IInkDrawingAttributes.RasterOperation, IInkDrawingAttributes.put_RasterOperation, IInkDrawingAttributes::RasterOperation, IInkDrawingAttributes::get_RasterOperation, IInkDrawingAttributes::put_RasterOperation, InkDrawingAttributes.get_RasterOperation, InkDrawingAttributes.put_RasterOperation, RasterOperation property [Tablet PC], RasterOperation property [Tablet PC],IInkDrawingAttributes interface, get_RasterOperation, msinkaut/IInkDrawingAttributes::RasterOperation, msinkaut/IInkDrawingAttributes::get_RasterOperation, msinkaut/IInkDrawingAttributes::put_RasterOperation, put_RasterOperation, tablet.inkdrawingattributes_rasteroperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkDrawingAttributes.RasterOperation
-	IInkDrawingAttributes.get_RasterOperation
-	IInkDrawingAttributes.put_RasterOperation
-	InkDrawingAttributes.get_RasterOperation
-	InkDrawingAttributes.put_RasterOperation
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

