---
UID: NF:msinkaut.IInkStrokeDisp.FindIntersections
title: IInkStrokeDisp::FindIntersections (msinkaut.h)
description: Retrieves the points where this IInkStrokeDisp object intersects other IInkStrokeDisp objects within a known InkStrokes collection.
helpviewer_keywords: ["FindIntersections","FindIntersections method [Tablet PC]","FindIntersections method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","FindIntersections method","IInkStrokeDisp.FindIntersections","IInkStrokeDisp::FindIntersections","a070fc87-608c-47be-b9b2-e2a41a31226f","msinkaut/IInkStrokeDisp::FindIntersections","tablet.iinkstrokedisp_findintersections"]
old-location: tablet\iinkstrokedisp_findintersections.htm
tech.root: tablet
ms.assetid: a070fc87-608c-47be-b9b2-e2a41a31226f
ms.date: 12/05/2018
ms.keywords: FindIntersections, FindIntersections method [Tablet PC], FindIntersections method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],FindIntersections method, IInkStrokeDisp.FindIntersections, IInkStrokeDisp::FindIntersections, a070fc87-608c-47be-b9b2-e2a41a31226f, msinkaut/IInkStrokeDisp::FindIntersections, tablet.iinkstrokedisp_findintersections
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
 - IInkStrokeDisp::FindIntersections
 - msinkaut/IInkStrokeDisp::FindIntersections
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
 - IInkStrokeDisp.FindIntersections
---

# IInkStrokeDisp::FindIntersections


## -description

Retrieves the points where this <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object intersects other <b>IInkStrokeDisp</b> objects within a known <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param Strokes [in]

 The known collection of strokes that are used to calculate the points where this stroke intersects strokes in the collection. If <b>NULL</b>, use all strokes in the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

<div class="alert"><b>Note</b>  The known collection of strokes must come from the same <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object as the stroke being tested for intersection. If it is not from the same <b>InkDisp</b> object, <b>E_INK_MISMATCHED_INK_OBJECT</b> is returned (see "HRESULT value" below). The <b>FindIntersections</b> method is the only Tablet PC application programming interface (API) that requires that the known collection of strokes come from the same <b>InkDisp</b> object.</div>
<div> </div>

### -param Intersections [out, retval]

When this method returns, contains an array of floating point index values that indicate the locations where this stroke intersects strokes within a known collection of strokes.

A floating point index is a float value that represents a location somewhere between two points in the stroke. As examples, if 0.0 is the first point in the stroke and 1.0 is the second point in the stroke, 0.5 is halfway between the first and second points. Similarly, a floating point index value of 37.25 represents a location that is 25 percent along the line between points 37 and 38 of the stroke.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> handle helper object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <i>strokes</i> parameter does not point to a compatible <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and this <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object don't match.

</td>
</tr>
</table>

## -remarks

This method can determine only the points of intersection.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getrectangleintersections">GetRectangleIntersections Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>