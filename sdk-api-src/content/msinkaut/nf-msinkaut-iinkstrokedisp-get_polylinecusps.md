---
UID: NF:msinkaut.IInkStrokeDisp.get_PolylineCusps
title: IInkStrokeDisp::get_PolylineCusps (msinkaut.h)
description: Gets an array that contains the indices of the cusps of the IInkStrokeDisp object.
helpviewer_keywords: ["67ae7265-4416-4eef-8a8f-85f3a5751200","IInkStrokeDisp interface [Tablet PC]","PolylineCusps property","IInkStrokeDisp.PolylineCusps","IInkStrokeDisp.get_PolylineCusps","IInkStrokeDisp::PolylineCusps","IInkStrokeDisp::get_PolylineCusps","PolylineCusps property [Tablet PC]","PolylineCusps property [Tablet PC]","IInkStrokeDisp interface","get_PolylineCusps","msinkaut/IInkStrokeDisp::PolylineCusps","msinkaut/IInkStrokeDisp::get_PolylineCusps","tablet.iinkstrokedisp_polylinecusps"]
old-location: tablet\iinkstrokedisp_polylinecusps.htm
tech.root: tablet
ms.assetid: 67ae7265-4416-4eef-8a8f-85f3a5751200
ms.date: 12/05/2018
ms.keywords: 67ae7265-4416-4eef-8a8f-85f3a5751200, IInkStrokeDisp interface [Tablet PC],PolylineCusps property, IInkStrokeDisp.PolylineCusps, IInkStrokeDisp.get_PolylineCusps, IInkStrokeDisp::PolylineCusps, IInkStrokeDisp::get_PolylineCusps, PolylineCusps property [Tablet PC], PolylineCusps property [Tablet PC],IInkStrokeDisp interface, get_PolylineCusps, msinkaut/IInkStrokeDisp::PolylineCusps, msinkaut/IInkStrokeDisp::get_PolylineCusps, tablet.iinkstrokedisp_polylinecusps
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
 - IInkStrokeDisp::get_PolylineCusps
 - msinkaut/IInkStrokeDisp::get_PolylineCusps
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
 - IInkStrokeDisp.PolylineCusps
 - IInkStrokeDisp.get_PolylineCusps
 - IInkStrokeDisp.get_PolylineCusps
---

# IInkStrokeDisp::get_PolylineCusps


## -description

Gets an array that contains the indices of the cusps of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.



This property is read-only.

## -parameters

## -remarks

The array returned by the <b>PolylineCusps</b> property is an index into the array returned by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpoints">GetPoints</a> method. Each index in the <b>PolylineCusps</b> property corresponds to a point in the array returned by the <b>GetPoints</b> method that is a cusp of the points of the stroke.

A cusp is a point on the stroke where the direction of writing changes in a discontinuous fashion. For example, if the stroke represents the capital letter "L", this property returns three cusps: two corresponding to the first and last control points on the stroke and the third representing the corner of the "L".

The location of a cusp can be determined by using the cusp as an index into the array returned by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpoints">GetPoints</a> method.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpoints">GetPoints Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>