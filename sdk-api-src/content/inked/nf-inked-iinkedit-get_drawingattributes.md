---
UID: NF:inked.IInkEdit.get_DrawingAttributes
title: IInkEdit::get_DrawingAttributes (inked.h)
description: Gets or sets the drawing attributes for ink that is yet to be drawn on the InkEdit control. (IInkEdit.get_DrawingAttributes)
helpviewer_keywords: ["8f5f00a2-abe1-487e-a067-2b6d929824c7","DrawingAttributes property [Tablet PC]","DrawingAttributes property [Tablet PC]","IInkEdit interface","IInkEdit interface [Tablet PC]","DrawingAttributes property","IInkEdit.DrawingAttributes","IInkEdit.get_DrawingAttributes","IInkEdit::DrawingAttributes","IInkEdit::get_DrawingAttributes","IInkEdit::putref_DrawingAttributes","InkEdit.get_DrawingAttributes","get_DrawingAttributes","inked/IInkEdit::DrawingAttributes","inked/IInkEdit::get_DrawingAttributes","inked/IInkEdit::putref_DrawingAttributes","put_DrawingAttributes","tablet.inkedit_drawingattributes"]
old-location: tablet\inkedit_drawingattributes.htm
tech.root: tablet
ms.assetid: 8f5f00a2-abe1-487e-a067-2b6d929824c7
ms.date: 12/05/2018
ms.keywords: 8f5f00a2-abe1-487e-a067-2b6d929824c7, DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],DrawingAttributes property, IInkEdit.DrawingAttributes, IInkEdit.get_DrawingAttributes, IInkEdit::DrawingAttributes, IInkEdit::get_DrawingAttributes, IInkEdit::putref_DrawingAttributes, InkEdit.get_DrawingAttributes, get_DrawingAttributes, inked/IInkEdit::DrawingAttributes, inked/IInkEdit::get_DrawingAttributes, inked/IInkEdit::putref_DrawingAttributes, put_DrawingAttributes, tablet.inkedit_drawingattributes
req.header: inked.h
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
req.lib: InkEd.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkEdit::get_DrawingAttributes
 - inked/IInkEdit::get_DrawingAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.DrawingAttributes
 - IInkEdit.get_DrawingAttributes
 - InkEdit.get_DrawingAttributes
---

# IInkEdit::get_DrawingAttributes


## -description

Gets or sets the drawing attributes for ink that is yet to be drawn on the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.



This property is read/write.

## -parameters

## -remarks

The <b>DrawingAttributes</b> property specifies the appearance of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object. For example, you can specify the width and color of ink drawn on the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

Successive calls to the <b>DrawingAttributes</b> property change only the <b>DrawingAttributes</b> properties of new <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects. The calls do not apply to <b>IInkStrokeDisp</b> objects that the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control already collected or is in the process of collecting.

This property is different from the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object, which specifies the attributes of already collected ink. The <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control's <b>DrawingAttributes</b> property is more analogous to the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes</a> property, except that for the <b>DefaultDrawingAttributes</b> property the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve">FitToCurve</a> property is set to <b>TRUE</b> by default.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
