---
UID: NF:msinkaut.IInkCursor.get_DrawingAttributes
title: IInkCursor::get_DrawingAttributes (msinkaut.h)
description: Gets or sets the drawing attributes to apply to ink as it is drawn. (IInkCursor.get_DrawingAttributes)
helpviewer_keywords: ["DrawingAttributes property [Tablet PC]","DrawingAttributes property [Tablet PC]","IInkCursor interface","IInkCursor interface [Tablet PC]","DrawingAttributes property","IInkCursor.DrawingAttributes","IInkCursor.get_DrawingAttributes","IInkCursor::DrawingAttributes","IInkCursor::get_DrawingAttributes","IInkCursor::putref_DrawingAttributes","de8b2473-092d-4ff9-adbc-3ba378b035e2","get_DrawingAttributes","msinkaut/IInkCursor::DrawingAttributes","msinkaut/IInkCursor::get_DrawingAttributes","msinkaut/IInkCursor::putref_DrawingAttributes","tablet.iinkcursor_drawingattributes"]
old-location: tablet\iinkcursor_drawingattributes.htm
tech.root: tablet
ms.assetid: de8b2473-092d-4ff9-adbc-3ba378b035e2
ms.date: 12/05/2018
ms.keywords: DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC],IInkCursor interface, IInkCursor interface [Tablet PC],DrawingAttributes property, IInkCursor.DrawingAttributes, IInkCursor.get_DrawingAttributes, IInkCursor::DrawingAttributes, IInkCursor::get_DrawingAttributes, IInkCursor::putref_DrawingAttributes, de8b2473-092d-4ff9-adbc-3ba378b035e2, get_DrawingAttributes, msinkaut/IInkCursor::DrawingAttributes, msinkaut/IInkCursor::get_DrawingAttributes, msinkaut/IInkCursor::putref_DrawingAttributes, tablet.iinkcursor_drawingattributes
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
 - IInkCursor::get_DrawingAttributes
 - msinkaut/IInkCursor::get_DrawingAttributes
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
 - IInkCursor.DrawingAttributes
 - IInkCursor.get_DrawingAttributes
 - IInkCursor.get_DrawingAttributes
---

# IInkCursor::get_DrawingAttributes


## -description

Gets or sets the drawing attributes to apply to ink as it is drawn.



This property is read/write.

## -parameters

## -remarks

The drawing attributes specify the appearance of the stroke. For example, you can specify the style and color of a pen.

A cursor can have different drawing attributes for each <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> with which it comes in contact. If you do not specify drawing attributes for a cursor, it uses the default drawing attributes of the <b>InkCollector</b> object. These default attributes are set with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes</a> property of the <b>InkCollector</b> object.

Successive calls to the <b>DrawingAttributes</b> property change only the drawing attributes of new strokes. They do not apply to strokes that are already collected or being collected.

<div class="alert"><b>Note</b>  This property behaves differently than the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes</a> property. Although the <b>DefaultDrawingAttributes</b> property specifies the drawing attributes that are applied to a new cursor, the <b>DrawingAttributes</b> property specifies the drawing attributes for ink that is yet to be collected.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes Property</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">InkCursor Interface</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>
