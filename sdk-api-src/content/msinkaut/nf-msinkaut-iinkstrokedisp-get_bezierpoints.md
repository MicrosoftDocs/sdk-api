---
UID: NF:msinkaut.IInkStrokeDisp.get_BezierPoints
title: IInkStrokeDisp::get_BezierPoints (msinkaut.h)
description: Gets the array of control points that represent the Bezier approximation of the stroke.
helpviewer_keywords: ["76bb749d-76cd-4c40-add3-4065d46ed6cb","BezierPoints property [Tablet PC]","BezierPoints property [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","BezierPoints property","IInkStrokeDisp.BezierPoints","IInkStrokeDisp.get_BezierPoints","IInkStrokeDisp::BezierPoints","IInkStrokeDisp::get_BezierPoints","get_BezierPoints","msinkaut/IInkStrokeDisp::BezierPoints","msinkaut/IInkStrokeDisp::get_BezierPoints","tablet.iinkstrokedisp_bezierpoints"]
old-location: tablet\iinkstrokedisp_bezierpoints.htm
tech.root: tablet
ms.assetid: 76bb749d-76cd-4c40-add3-4065d46ed6cb
ms.date: 12/05/2018
ms.keywords: 76bb749d-76cd-4c40-add3-4065d46ed6cb, BezierPoints property [Tablet PC], BezierPoints property [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],BezierPoints property, IInkStrokeDisp.BezierPoints, IInkStrokeDisp.get_BezierPoints, IInkStrokeDisp::BezierPoints, IInkStrokeDisp::get_BezierPoints, get_BezierPoints, msinkaut/IInkStrokeDisp::BezierPoints, msinkaut/IInkStrokeDisp::get_BezierPoints, tablet.iinkstrokedisp_bezierpoints
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
 - IInkStrokeDisp::get_BezierPoints
 - msinkaut/IInkStrokeDisp::get_BezierPoints
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
 - IInkStrokeDisp.BezierPoints
 - IInkStrokeDisp.get_BezierPoints
 - IInkStrokeDisp.get_BezierPoints
---

# IInkStrokeDisp::get_BezierPoints


## -description

Gets the array of control points that represent the Bezier approximation of the stroke.



This property is read-only.

## -parameters

## -remarks

The control points that the <b>BezierPoints</b> property returns provide a smooth approximation of the original stroke and do not necessarily lie on the stroke.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_beziercusps">BezierCusps Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>