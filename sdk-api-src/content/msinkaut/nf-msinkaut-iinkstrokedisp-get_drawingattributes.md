---
UID: NF:msinkaut.IInkStrokeDisp.get_DrawingAttributes
title: IInkStrokeDisp::get_DrawingAttributes (msinkaut.h)
description: Gets or sets the drawing attributes to apply to ink as it is drawn. (IInkStrokeDisp.get_DrawingAttributes)
helpviewer_keywords: ["DrawingAttributes property [Tablet PC]","DrawingAttributes property [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","DrawingAttributes property","IInkStrokeDisp.DrawingAttributes","IInkStrokeDisp.get_DrawingAttributes","IInkStrokeDisp.put_DrawingAttributes","IInkStrokeDisp::DrawingAttributes","IInkStrokeDisp::get_DrawingAttributes","IInkStrokeDisp::put_DrawingAttributes","get_DrawingAttributes","msinkaut/IInkStrokeDisp::DrawingAttributes","msinkaut/IInkStrokeDisp::get_DrawingAttributes","msinkaut/IInkStrokeDisp::put_DrawingAttributes","tablet.iinkstrokedisp_drawingattributes"]
old-location: tablet\iinkstrokedisp_drawingattributes.htm
tech.root: tablet
ms.assetid: f41de939-0c20-4128-bee4-22a0c434159f
ms.date: 12/05/2018
ms.keywords: DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],DrawingAttributes property, IInkStrokeDisp.DrawingAttributes, IInkStrokeDisp.get_DrawingAttributes, IInkStrokeDisp.put_DrawingAttributes, IInkStrokeDisp::DrawingAttributes, IInkStrokeDisp::get_DrawingAttributes, IInkStrokeDisp::put_DrawingAttributes, get_DrawingAttributes, msinkaut/IInkStrokeDisp::DrawingAttributes, msinkaut/IInkStrokeDisp::get_DrawingAttributes, msinkaut/IInkStrokeDisp::put_DrawingAttributes, tablet.iinkstrokedisp_drawingattributes
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
 - IInkStrokeDisp::get_DrawingAttributes
 - msinkaut/IInkStrokeDisp::get_DrawingAttributes
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
 - IInkStrokeDisp.DrawingAttributes
 - IInkStrokeDisp.get_DrawingAttributes
 - IInkStrokeDisp.put_DrawingAttributes
 - IInkStrokeDisp.get_DrawingAttributes
 - IInkStrokeDisp.put_DrawingAttributes
---

# IInkStrokeDisp::get_DrawingAttributes


## -description

Gets or sets the drawing attributes to apply to ink as it is drawn.



This property is read/write.

## -parameters

## -remarks

The drawing attributes specify the appearance of the stroke. For example, you can specify the style and color of a pen.

A cursor can have different drawing attributes for each <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> with which it comes in contact. If you do not specify drawing attributes for a cursor, it uses the default drawing attributes of the <b>InkCollector</b> object. These default attributes are set with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes</a> property of the <b>InkCollector</b> object.

Successive calls to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property change only the drawing attributes of new strokes. They do not apply to strokes that are already collected or being collected.

<div class="alert"><b>Note</b>  This property behaves differently than the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes</a> property. Although the <b>DefaultDrawingAttributes</b> property specifies the drawing attributes that are applied to a new cursor, the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property specifies the drawing attributes for ink that is yet to be collected.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>
