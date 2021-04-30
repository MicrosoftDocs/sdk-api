---
UID: NF:msinkaut.IInkStrokeDisp.get_BezierCusps
title: IInkStrokeDisp::get_BezierCusps (msinkaut.h)
description: Gets an array that contains the indices of the cusps of the Bezier approximation of the stroke.
helpviewer_keywords: ["9fdd007a-1c8e-4389-975c-849a67be94a1","BezierCusps property [Tablet PC]","BezierCusps property [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","BezierCusps property","IInkStrokeDisp.BezierCusps","IInkStrokeDisp.get_BezierCusps","IInkStrokeDisp::BezierCusps","IInkStrokeDisp::get_BezierCusps","get_BezierCusps","msinkaut/IInkStrokeDisp::BezierCusps","msinkaut/IInkStrokeDisp::get_BezierCusps","tablet.iinkstrokedisp_beziercusps"]
old-location: tablet\iinkstrokedisp_beziercusps.htm
tech.root: tablet
ms.assetid: 9fdd007a-1c8e-4389-975c-849a67be94a1
ms.date: 12/05/2018
ms.keywords: 9fdd007a-1c8e-4389-975c-849a67be94a1, BezierCusps property [Tablet PC], BezierCusps property [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],BezierCusps property, IInkStrokeDisp.BezierCusps, IInkStrokeDisp.get_BezierCusps, IInkStrokeDisp::BezierCusps, IInkStrokeDisp::get_BezierCusps, get_BezierCusps, msinkaut/IInkStrokeDisp::BezierCusps, msinkaut/IInkStrokeDisp::get_BezierCusps, tablet.iinkstrokedisp_beziercusps
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
 - IInkStrokeDisp::get_BezierCusps
 - msinkaut/IInkStrokeDisp::get_BezierCusps
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
 - IInkStrokeDisp.BezierCusps
 - IInkStrokeDisp.get_BezierCusps
 - IInkStrokeDisp.get_BezierCusps
---

# IInkStrokeDisp::get_BezierCusps


## -description

Gets an array that contains the indices of the <b>cusps</b> of the Bezier approximation of the stroke.



This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The array of Bezier control points that the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_bezierpoints">BezierPoints</a> property returns are made up of x and y values. The <b>BezierCusps</b> property refers only to the x values in this array. The y values can be retrieved by an action similar to the following below.</div>
<div> </div>
A cusp is a point on the stroke where the direction of writing changes in a discontinuous fashion. For example, if the stroke represents the capital letter "L", this property returns three cusps: two corresponding to the first and last control points on the stroke and the third representing the corner of the "L".

The following code extracts the x and y values of the Bezier cusps of an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a>, <code>theStroke</code>, and stores them in a two-dimensional array called <code>BezierCuspValues</code>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_bezierpoints">BezierPoints Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>