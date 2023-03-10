---
UID: NF:msinkaut15.IInkDivisionResult.get_Strokes
title: IInkDivisionResult::get_Strokes (msinkaut15.h)
description: Gets the collection of strokes that are contained in an object or used to create an object. (IInkDivisionResult.get_Strokes)
helpviewer_keywords: ["IInkDivisionResult interface [Tablet PC]","Strokes property","IInkDivisionResult.Strokes","IInkDivisionResult.get_Strokes","IInkDivisionResult::Strokes","IInkDivisionResult::get_Strokes","Strokes property [Tablet PC]","Strokes property [Tablet PC]","IInkDivisionResult interface","b65f1b71-b0a4-4de2-9321-f660bcd2d3ce","get_Strokes","msinkaut15/IInkDivisionResult::Strokes","msinkaut15/IInkDivisionResult::get_Strokes","tablet.iinkdivisionresult_strokes"]
old-location: tablet\iinkdivisionresult_strokes.htm
tech.root: tablet
ms.assetid: b65f1b71-b0a4-4de2-9321-f660bcd2d3ce
ms.date: 12/05/2018
ms.keywords: IInkDivisionResult interface [Tablet PC],Strokes property, IInkDivisionResult.Strokes, IInkDivisionResult.get_Strokes, IInkDivisionResult::Strokes, IInkDivisionResult::get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkDivisionResult interface, b65f1b71-b0a4-4de2-9321-f660bcd2d3ce, get_Strokes, msinkaut15/IInkDivisionResult::Strokes, msinkaut15/IInkDivisionResult::get_Strokes, tablet.iinkdivisionresult_strokes
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDivisionResult::get_Strokes
 - msinkaut15/IInkDivisionResult::get_Strokes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionResult.Strokes
 - IInkDivisionResult.get_Strokes
 - IInkDivisionResult.get_Strokes
---

# IInkDivisionResult::get_Strokes


## -description

Gets the collection of strokes that are contained in an object or used to create an object.



This property is read-only.

## -parameters

## -remarks

The collection of strokes may be the copies of the strokes contained in an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object or the strokes that were used to create the object or collection.

<div class="alert"><b>Note</b>  The <b>Strokes</b> property for the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object does not return the actual collection that the <b>InkDisp</b> object works with, but instead returns a copy. For example, this means that adding or removing strokes to this collection does not affect the <b>InkDisp</b> object's strokes; to add or remove strokes, use <b>InkDisp</b> methods such as <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle">AddStrokesAtRectangle</a>, <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke">DeleteStroke</a>, and <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a>. However, each stroke in the collection is a reference to the original <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
