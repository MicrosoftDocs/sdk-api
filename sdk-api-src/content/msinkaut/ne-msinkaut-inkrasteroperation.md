---
UID: NE:msinkaut.InkRasterOperation
title: InkRasterOperation
author: windows-sdk-content
description: Defines values for performing raster operations on drawn ink.
old-location: tablet\inkrasteroperation.htm
old-project: tablet
ms.assetid: 34403724-b883-4c03-8784-fe8f205d3da6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 34403724-b883-4c03-8784-fe8f205d3da6, IRO_Black, IRO_CopyPen, IRO_MaskNotPen, IRO_MaskPen, IRO_MaskPenNot, IRO_MergeNotPen, IRO_MergePen, IRO_MergePenNot, IRO_NoOperation, IRO_Not, IRO_NotCopyPen, IRO_NotMaskPen, IRO_NotMergePen, IRO_NotXOrPen, IRO_White, IRO_XOrPen, InkRasterOperation, InkRasterOperation enumeration [Tablet PC], msinkaut/IRO_Black, msinkaut/IRO_CopyPen, msinkaut/IRO_MaskNotPen, msinkaut/IRO_MaskPen, msinkaut/IRO_MaskPenNot, msinkaut/IRO_MergeNotPen, msinkaut/IRO_MergePen, msinkaut/IRO_MergePenNot, msinkaut/IRO_NoOperation, msinkaut/IRO_Not, msinkaut/IRO_NotCopyPen, msinkaut/IRO_NotMaskPen, msinkaut/IRO_NotMergePen, msinkaut/IRO_NotXOrPen, msinkaut/IRO_White, msinkaut/IRO_XOrPen, msinkaut/InkRasterOperation, tablet.inkrasteroperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: InkRasterOperation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkRasterOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InkRasterOperation enumeration


## -description



Defines values for performing raster operations on drawn ink.




## -enum-fields




### -field IRO_Black

 Black pen color.


### -field IRO_NotMergePen

The  inverse of MergePen.


### -field IRO_MaskNotPen

 A combination of the colors that are common to the background color and the inverse of the pen.


### -field IRO_NotCopyPen

 The inverse of CopyPen.


### -field IRO_MaskPenNot

A combination of the colors that are common to both the pen and the inverse of the display.


### -field IRO_Not

The inverse of the display color.


### -field IRO_XOrPen

A combination of the colors in the pen and in the display color, but not in both.


### -field IRO_NotMaskPen

The inverse of MaskPen.


### -field IRO_MaskPen

A combination of the colors that are common to both the pen and the display.


### -field IRO_NotXOrPen

An inverse of XOrPen.


### -field IRO_NoOperation

No operation; the output remains unchanged.


### -field IRO_MergeNotPen

A combination of the display color and the inverse of the pen color.


### -field IRO_CopyPen

The pen color.

This is the default value.


### -field IRO_MergePenNot

A combination of the pen color and the inverse of the display color.


### -field IRO_MergePen

A combination of the pen color and the display color.


### -field IRO_White

A white pen color.


## -remarks



Use these values to set the value for the <a href="https://msdn.microsoft.com/8e3681a7-c5be-4104-b740-9f23d141f6cb">RasterOperation</a> drawing attribute. Any object with a <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property can have this value set.

<div class="alert"><b>Note</b>  Many printers do not support many of the available raster operations. Because of this, the colors you see on the display may be different from the colors that you would see if they were printed on paper. This is directly related to the printer drivers or printer hardware. You may need to experiment to determine which printers can produce the correct output when various raster operations are set on ink.</div>
<div> </div>
When the <b>RasterOperation</b> value is set to anything other than CopyPen, all drawing attributes (anti-aliasing, smoothing, transparency, and pressure) are ignored.




## -see-also




<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/8e3681a7-c5be-4104-b740-9f23d141f6cb">RasterOperation Property</a>
 

 

