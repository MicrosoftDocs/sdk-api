---
UID: NF:msinkaut.IInkPicture.get_DefaultDrawingAttributes
title: IInkPicture::get_DefaultDrawingAttributes (msinkaut.h)
description: Gets or sets the default drawing attributes to use when drawing and displaying ink.
helpviewer_keywords: ["DefaultDrawingAttributes property [Tablet PC]","DefaultDrawingAttributes property [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","DefaultDrawingAttributes property","IInkPicture.DefaultDrawingAttributes","IInkPicture.get_DefaultDrawingAttributes","IInkPicture::DefaultDrawingAttributes","IInkPicture::get_DefaultDrawingAttributes","IInkPicture::put_DefaultDrawingAttributes","InkPicture.get_DefaultDrawingAttributes","InkPicture.put_DefaultDrawingAttributes","get_DefaultDrawingAttributes","msinkaut/IInkPicture::DefaultDrawingAttributes","msinkaut/IInkPicture::get_DefaultDrawingAttributes","msinkaut/IInkPicture::put_DefaultDrawingAttributes","putref_DefaultDrawingAttributes","tablet.inkpicture_defaultdrawingattributes"]
old-location: tablet\inkpicture_defaultdrawingattributes.htm
tech.root: tablet
ms.assetid: 9a4dff66-9789-4979-947e-73bbf85cece2
ms.date: 12/05/2018
ms.keywords: DefaultDrawingAttributes property [Tablet PC], DefaultDrawingAttributes property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],DefaultDrawingAttributes property, IInkPicture.DefaultDrawingAttributes, IInkPicture.get_DefaultDrawingAttributes, IInkPicture::DefaultDrawingAttributes, IInkPicture::get_DefaultDrawingAttributes, IInkPicture::put_DefaultDrawingAttributes, InkPicture.get_DefaultDrawingAttributes, InkPicture.put_DefaultDrawingAttributes, get_DefaultDrawingAttributes, msinkaut/IInkPicture::DefaultDrawingAttributes, msinkaut/IInkPicture::get_DefaultDrawingAttributes, msinkaut/IInkPicture::put_DefaultDrawingAttributes, putref_DefaultDrawingAttributes, tablet.inkpicture_defaultdrawingattributes
f1_keywords:
- msinkaut/IInkPicture.DefaultDrawingAttributes
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkPicture.DefaultDrawingAttributes
- IInkPicture.get_DefaultDrawingAttributes
- IInkPicture.put_DefaultDrawingAttributes
- InkPicture.get_DefaultDrawingAttributes
- InkPicture.put_DefaultDrawingAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkPicture::get_DefaultDrawingAttributes


## -description



Gets or sets the default drawing attributes to use when drawing and displaying ink.



This property is read/write.


## -parameters


## -remarks



The drawing attributes specified with this property are the attributes that are assigned to a new cursor.

The default drawing attributes are as follows:


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased">AntiAliased</a> = <b>TRUE</b>


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color</a> = <b>BLACK</b> (RGB(0,0,0)) if not in High Contrast mode; otherwise, Color=COLOR_WINDOWTEXT.


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve">FitToCurve</a> = <b>FALSE</b>


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height">Height</a> = 1 (in ink space units)


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure">IgnorePressure</a> = <b>FALSE</b>


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip">PenTip</a> = <b>Ball</b>


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation">RasterOperation</a> = <b>CopyPen</b>


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency">Transparency</a> = 0 (totally opaque)


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width</a> = 53 (in ink space units)

To set different attributes on a new cursor, use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object.

To change the drawing attributes of a single stroke, use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object. To change the drawing attributes of a collection of strokes, call the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes">ModifyDrawingAttributes</a> method of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

<div class="alert"><b>Note</b>  The <b>DefaultDrawingAttributes</b> property contains the drawing attributes that all cursors use unless they set their own <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property. For example, a new <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object uses <b>DefaultDrawingAttributes</b>, and an old <b>IInkCursor</b> object on which the <b>DrawingAttributes</b> is set to <b>NULL</b> also uses <b>DefaultDrawingAttributes</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes">ModifyDrawingAttributes Method</a>
 

 

