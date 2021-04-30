---
UID: NF:msinkaut.IInkStrokeDisp.NearestPoint
title: IInkStrokeDisp::NearestPoint (msinkaut.h)
description: Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates.
helpviewer_keywords: ["87c01f9d-b48a-459c-99f8-9634e1693fa0","IInkStrokeDisp interface [Tablet PC]","NearestPoint method","IInkStrokeDisp.NearestPoint","IInkStrokeDisp::NearestPoint","NearestPoint","NearestPoint method [Tablet PC]","NearestPoint method [Tablet PC]","IInkStrokeDisp interface","msinkaut/IInkStrokeDisp::NearestPoint","tablet.iinkstrokedisp_nearestpoint"]
old-location: tablet\iinkstrokedisp_nearestpoint.htm
tech.root: tablet
ms.assetid: 87c01f9d-b48a-459c-99f8-9634e1693fa0
ms.date: 12/05/2018
ms.keywords: 87c01f9d-b48a-459c-99f8-9634e1693fa0, IInkStrokeDisp interface [Tablet PC],NearestPoint method, IInkStrokeDisp.NearestPoint, IInkStrokeDisp::NearestPoint, NearestPoint, NearestPoint method [Tablet PC], NearestPoint method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::NearestPoint, tablet.iinkstrokedisp_nearestpoint
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
 - IInkStrokeDisp::NearestPoint
 - msinkaut/IInkStrokeDisp::NearestPoint
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
 - IInkStrokeDisp.NearestPoint
---

# IInkStrokeDisp::NearestPoint


## -description

Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates.

## -parameters

### -param X [in]

The x-position in ink space of the point to test.

### -param Y [in]

The y-position in ink space of the point to test.

### -param Distance [in, out, optional]

Optional. The distance from the point to the stroke. This parameter can be <b>NULL</b>. The default value is 0.

### -param Point [out, retval]

When this method returns, contains the floating point index value that represents the closest location on the stroke.

A floating point index is a float value that represents a location somewhere between two points in the stroke. As examples, if 0.0 is the first point in the stroke and 1.0 is the second point in the stroke, 0.5 is halfway between the first and second points. Similarly, a floating point index value of 37.25 represents a location that is 25 percent along the line between points 37 and 38 of the stroke.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -remarks

The <i>distance</i> parameter describes the distance from the point to the envelope of the stroke. This is the distance between the two points minus half the width of the stroke.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getrectangleintersections">GetRectangleIntersections Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle">HitTest(Point, Single) Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint">NearestPoint Method [InkDisp Class]</a>