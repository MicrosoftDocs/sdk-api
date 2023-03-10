---
UID: NF:msinkaut.IInkStrokeDisp.get_SelfIntersections
title: IInkStrokeDisp::get_SelfIntersections (msinkaut.h)
description: Gets the self-intersections of the stroke.
helpviewer_keywords: ["IInkStrokeDisp interface [Tablet PC]","SelfIntersections property","IInkStrokeDisp.SelfIntersections","IInkStrokeDisp.get_SelfIntersections","IInkStrokeDisp::SelfIntersections","IInkStrokeDisp::get_SelfIntersections","SelfIntersections property [Tablet PC]","SelfIntersections property [Tablet PC]","IInkStrokeDisp interface","d3b97071-d0bd-4910-93a4-409241e427eb","get_SelfIntersections","msinkaut/IInkStrokeDisp::SelfIntersections","msinkaut/IInkStrokeDisp::get_SelfIntersections","tablet.iinkstrokedisp_selfintersections"]
old-location: tablet\iinkstrokedisp_selfintersections.htm
tech.root: tablet
ms.assetid: d3b97071-d0bd-4910-93a4-409241e427eb
ms.date: 12/05/2018
ms.keywords: IInkStrokeDisp interface [Tablet PC],SelfIntersections property, IInkStrokeDisp.SelfIntersections, IInkStrokeDisp.get_SelfIntersections, IInkStrokeDisp::SelfIntersections, IInkStrokeDisp::get_SelfIntersections, SelfIntersections property [Tablet PC], SelfIntersections property [Tablet PC],IInkStrokeDisp interface, d3b97071-d0bd-4910-93a4-409241e427eb, get_SelfIntersections, msinkaut/IInkStrokeDisp::SelfIntersections, msinkaut/IInkStrokeDisp::get_SelfIntersections, tablet.iinkstrokedisp_selfintersections
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
 - IInkStrokeDisp::get_SelfIntersections
 - msinkaut/IInkStrokeDisp::get_SelfIntersections
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
 - IInkStrokeDisp.SelfIntersections
 - IInkStrokeDisp.get_SelfIntersections
 - IInkStrokeDisp.get_SelfIntersections
---

# IInkStrokeDisp::get_SelfIntersections


## -description

Gets the self-intersections of the stroke.



This property is read-only.

## -parameters

## -remarks

A self-intersection is the point of a stroke where the stroke crosses over itself.

A floating point index is a float value that represents a location somewhere between two points in the stroke. As examples, if 0.0 is the first point in the stroke and 1.0 is the second point in the stroke, 0.5 is halfway between the first and second points. Similarly, a floating point index value of 37.25 represents a location that is 25 percent along the line between points 37 and 38 of the stroke.

<div class="alert"><b>Note</b>  A floating point index is returned for each intersection and line segment combination. If a stroke has one intersection, this property returns two self intersections, one for each line segment that is part of the intersection.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>