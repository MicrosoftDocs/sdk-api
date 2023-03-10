---
UID: NF:msinkaut.IInkDisp.HitTestCircle
title: IInkDisp::HitTestCircle (msinkaut.h)
description: Retrieves the InkStrokes collection that are either completely inside or intersected by a known circle.
helpviewer_keywords: ["2025f728-cb08-4285-8584-c9ad537e58f2","HitTestCircle","HitTestCircle method [Tablet PC]","HitTestCircle method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","HitTestCircle method","IInkDisp.HitTestCircle","IInkDisp::HitTestCircle","msinkaut/IInkDisp::HitTestCircle","tablet.inkdisp_hittest_point__single"]
old-location: tablet\inkdisp_hittest_point__single.htm
tech.root: tablet
ms.assetid: 2025f728-cb08-4285-8584-c9ad537e58f2
ms.date: 12/05/2018
ms.keywords: 2025f728-cb08-4285-8584-c9ad537e58f2, HitTestCircle, HitTestCircle method [Tablet PC], HitTestCircle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],HitTestCircle method, IInkDisp.HitTestCircle, IInkDisp::HitTestCircle, msinkaut/IInkDisp::HitTestCircle, tablet.inkdisp_hittest_point__single
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
 - IInkDisp::HitTestCircle
 - msinkaut/IInkDisp::HitTestCircle
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
 - IInkDisp.HitTestCircle
---

# IInkDisp::HitTestCircle


## -description

Retrieves the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that are either completely inside or intersected by a known circle.

## -parameters

### -param X [in]

The x-position of the center of the hit test circle in ink space units.

### -param Y [in]

The y-position of the center of the hit test circle in ink space units.

### -param radius [in]

The radius of the circle to use in the hit test, in ink space units.

### -param Strokes [out, retval]

When this method returns, contains the collection of strokes that are either completely inside or intersected by the specified circle.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid display handle.

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
</table>

## -remarks

If a stroke intersects the circle, the complete stroke is returned.

The method computes the intersection, considering the full set of drawing attributes that apply to the stroke, including the full pen width, Bezier smoothing (if present), and shape of the pen tip.

After a rotation or shear transform has been performed on a stroke or a collection of strokes, the transformed <code>x-</code> and <code>y-</code> coordinates are no longer concentric with the original coordinates. Because of this, the <code>radius</code> argument should not be calculated from the <code>x-</code> or <code>y-</code> coordinates.

To determine which points of a known stroke intersect the test area, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-hittestcircle">HitTest</a> method of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.

The application must always pass in a destination pointer for the resulting collection of strokes. If there are no intersections, the collection has a count of zero.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso">HitTest(Point[], Single) Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle">HitTest(Rectangle, Single) Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
