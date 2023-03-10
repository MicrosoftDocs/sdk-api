---
UID: NF:msinkaut.IInkDrawingAttributes.put_RasterOperation
title: IInkDrawingAttributes::put_RasterOperation (msinkaut.h)
description: Gets or sets a value that defines how the colors of the pen and background interact. (Put)
helpviewer_keywords: ["8e3681a7-c5be-4104-b740-9f23d141f6cb","IInkDrawingAttributes interface [Tablet PC]","RasterOperation property","IInkDrawingAttributes.RasterOperation","IInkDrawingAttributes.put_RasterOperation","IInkDrawingAttributes::RasterOperation","IInkDrawingAttributes::get_RasterOperation","IInkDrawingAttributes::put_RasterOperation","InkDrawingAttributes.get_RasterOperation","InkDrawingAttributes.put_RasterOperation","RasterOperation property [Tablet PC]","RasterOperation property [Tablet PC]","IInkDrawingAttributes interface","get_RasterOperation","msinkaut/IInkDrawingAttributes::RasterOperation","msinkaut/IInkDrawingAttributes::get_RasterOperation","msinkaut/IInkDrawingAttributes::put_RasterOperation","put_RasterOperation","tablet.inkdrawingattributes_rasteroperation"]
old-location: tablet\inkdrawingattributes_rasteroperation.htm
tech.root: tablet
ms.assetid: 8e3681a7-c5be-4104-b740-9f23d141f6cb
ms.date: 12/05/2018
ms.keywords: 8e3681a7-c5be-4104-b740-9f23d141f6cb, IInkDrawingAttributes interface [Tablet PC],RasterOperation property, IInkDrawingAttributes.RasterOperation, IInkDrawingAttributes.put_RasterOperation, IInkDrawingAttributes::RasterOperation, IInkDrawingAttributes::get_RasterOperation, IInkDrawingAttributes::put_RasterOperation, InkDrawingAttributes.get_RasterOperation, InkDrawingAttributes.put_RasterOperation, RasterOperation property [Tablet PC], RasterOperation property [Tablet PC],IInkDrawingAttributes interface, get_RasterOperation, msinkaut/IInkDrawingAttributes::RasterOperation, msinkaut/IInkDrawingAttributes::get_RasterOperation, msinkaut/IInkDrawingAttributes::put_RasterOperation, put_RasterOperation, tablet.inkdrawingattributes_rasteroperation
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDrawingAttributes::put_RasterOperation
 - msinkaut/IInkDrawingAttributes::put_RasterOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDrawingAttributes.RasterOperation
 - IInkDrawingAttributes.get_RasterOperation
 - IInkDrawingAttributes.put_RasterOperation
 - InkDrawingAttributes.get_RasterOperation
 - InkDrawingAttributes.put_RasterOperation
---

# IInkDrawingAttributes::put_RasterOperation


## -description

Gets or sets a value that defines how the colors of the pen and background interact.



This property is read/write.

## -parameters

## -remarks

The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrasteroperation">InkRasterOperation</a> enumeration defines values for performing raster operations on drawn ink. For example, if you want to perform subtractive transparency, set the raster value to MaskPen.

For a complete list of available raster operations, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrasteroperation">InkRasterOperation</a> enumeration type.

<div class="alert"><b>Note</b>  Many printers do not support many of the available raster operations. Because of this, the colors displayed may be different than the colors printed. This is directly related to the printer drivers or printer hardware. You may have to experiment to determine which printers can produce the correct output when various raster operations are set on ink.</div>
<div> </div>
When the <b>RasterOperation</b> property is set to anything other than <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrasteroperation">InkRasterOperation.IRO_CopyPen</a>, all drawing attributes-anti-aliasing, smoothing, transparency, and pressure-are ignored.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdrawingattributes.md">IInkDrawingAttributes</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrasteroperation">InkRasterOperation Enumeration</a>
