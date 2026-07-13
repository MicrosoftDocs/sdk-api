---
UID: NE:msinkaut.InkRasterOperation
title: InkRasterOperation (msinkaut.h)
description: Defines values for performing raster operations on drawn ink.
helpviewer_keywords: ["34403724-b883-4c03-8784-fe8f205d3da6","IRO_Black","IRO_CopyPen","IRO_MaskNotPen","IRO_MaskPen","IRO_MaskPenNot","IRO_MergeNotPen","IRO_MergePen","IRO_MergePenNot","IRO_NoOperation","IRO_Not","IRO_NotCopyPen","IRO_NotMaskPen","IRO_NotMergePen","IRO_NotXOrPen","IRO_White","IRO_XOrPen","InkRasterOperation","InkRasterOperation enumeration [Tablet PC]","msinkaut/IRO_Black","msinkaut/IRO_CopyPen","msinkaut/IRO_MaskNotPen","msinkaut/IRO_MaskPen","msinkaut/IRO_MaskPenNot","msinkaut/IRO_MergeNotPen","msinkaut/IRO_MergePen","msinkaut/IRO_MergePenNot","msinkaut/IRO_NoOperation","msinkaut/IRO_Not","msinkaut/IRO_NotCopyPen","msinkaut/IRO_NotMaskPen","msinkaut/IRO_NotMergePen","msinkaut/IRO_NotXOrPen","msinkaut/IRO_White","msinkaut/IRO_XOrPen","msinkaut/InkRasterOperation","tablet.inkrasteroperation"]
old-location: tablet\inkrasteroperation.htm
tech.root: tablet
ms.assetid: 34403724-b883-4c03-8784-fe8f205d3da6
ms.date: 12/05/2018
ms.keywords: 34403724-b883-4c03-8784-fe8f205d3da6, IRO_Black, IRO_CopyPen, IRO_MaskNotPen, IRO_MaskPen, IRO_MaskPenNot, IRO_MergeNotPen, IRO_MergePen, IRO_MergePenNot, IRO_NoOperation, IRO_Not, IRO_NotCopyPen, IRO_NotMaskPen, IRO_NotMergePen, IRO_NotXOrPen, IRO_White, IRO_XOrPen, InkRasterOperation, InkRasterOperation enumeration [Tablet PC], msinkaut/IRO_Black, msinkaut/IRO_CopyPen, msinkaut/IRO_MaskNotPen, msinkaut/IRO_MaskPen, msinkaut/IRO_MaskPenNot, msinkaut/IRO_MergeNotPen, msinkaut/IRO_MergePen, msinkaut/IRO_MergePenNot, msinkaut/IRO_NoOperation, msinkaut/IRO_Not, msinkaut/IRO_NotCopyPen, msinkaut/IRO_NotMaskPen, msinkaut/IRO_NotMergePen, msinkaut/IRO_NotXOrPen, msinkaut/IRO_White, msinkaut/IRO_XOrPen, msinkaut/InkRasterOperation, tablet.inkrasteroperation
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: InkRasterOperation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkRasterOperation
 - msinkaut/InkRasterOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkRasterOperation
---

# InkRasterOperation enumeration


## -description

Defines values for performing raster operations on drawn ink.

## -enum-fields

### -field IRO_Black:1

 Black pen color.

### -field IRO_NotMergePen:2

The  inverse of MergePen.

### -field IRO_MaskNotPen:3

 A combination of the colors that are common to the background color and the inverse of the pen.

### -field IRO_NotCopyPen:4

 The inverse of CopyPen.

### -field IRO_MaskPenNot:5

A combination of the colors that are common to both the pen and the inverse of the display.

### -field IRO_Not:6

The inverse of the display color.

### -field IRO_XOrPen:7

A combination of the colors in the pen and in the display color, but not in both.

### -field IRO_NotMaskPen:8

The inverse of MaskPen.

### -field IRO_MaskPen:9

A combination of the colors that are common to both the pen and the display.

### -field IRO_NotXOrPen:10

An inverse of XOrPen.

### -field IRO_NoOperation:11

No operation; the output remains unchanged.

### -field IRO_MergeNotPen:12

A combination of the display color and the inverse of the pen color.

### -field IRO_CopyPen:13

The pen color.

This is the default value.

### -field IRO_MergePenNot:14

A combination of the pen color and the inverse of the display color.

### -field IRO_MergePen:15

A combination of the pen color and the display color.

### -field IRO_White:16

A white pen color.

## -remarks

Use these values to set the value for the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation">RasterOperation</a> drawing attribute. Any object with a <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property can have this value set.

<div class="alert"><b>Note</b>  Many printers do not support many of the available raster operations. Because of this, the colors you see on the display may be different from the colors that you would see if they were printed on paper. This is directly related to the printer drivers or printer hardware. You may need to experiment to determine which printers can produce the correct output when various raster operations are set on ink.</div>
<div> </div>
When the <b>RasterOperation</b> value is set to anything other than CopyPen, all drawing attributes (anti-aliasing, smoothing, transparency, and pressure) are ignored.

## -see-also

<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation">RasterOperation Property</a>
