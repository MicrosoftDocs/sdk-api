---
UID: NF:msinkaut.IInkDisp.HitTestWithRectangle
title: IInkDisp::HitTestWithRectangle (msinkaut.h)
description: Retrieves the strokes that are contained within a specified rectangle.
helpviewer_keywords: ["401c4f62-a406-49ac-9911-91f815cde9c8","HitTestWithRectangle","HitTestWithRectangle method [Tablet PC]","HitTestWithRectangle method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","HitTestWithRectangle method","IInkDisp.HitTestWithRectangle","IInkDisp::HitTestWithRectangle","msinkaut/IInkDisp::HitTestWithRectangle","tablet.inkdisp_hittest_rectangle__single"]
old-location: tablet\inkdisp_hittest_rectangle__single.htm
tech.root: tablet
ms.assetid: 401c4f62-a406-49ac-9911-91f815cde9c8
ms.date: 12/05/2018
ms.keywords: 401c4f62-a406-49ac-9911-91f815cde9c8, HitTestWithRectangle, HitTestWithRectangle method [Tablet PC], HitTestWithRectangle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],HitTestWithRectangle method, IInkDisp.HitTestWithRectangle, IInkDisp::HitTestWithRectangle, msinkaut/IInkDisp::HitTestWithRectangle, tablet.inkdisp_hittest_rectangle__single
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
 - IInkDisp::HitTestWithRectangle
 - msinkaut/IInkDisp::HitTestWithRectangle
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
 - IInkDisp.HitTestWithRectangle
---

# IInkDisp::HitTestWithRectangle


## -description

Retrieves the strokes that are contained within a specified rectangle.

## -parameters

### -param SelectionRectangle [in]

The selection rectangle, of type <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a>, in ink space coordinates.

### -param IntersectPercent [in]

The float or single percentage value that determines which strokes are included in the collection. Strokes that intersect the rectangle are included in the collection if the percentage of points in those strokes contained within the rectangle is greater than or equal to the <i>IntersectPercent</i> percentage.

### -param Strokes [out, retval]

When this method returns, contains a pointer to the collection of strokes that makes up the ink.

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
</table>

## -remarks

To determine which points of a known stroke intersect the test area, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getrectangleintersections">GetRectangleIntersections</a> method of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object, which retrieves the points where a stroke intersects a known rectangle.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle">HitTest(Point, Single) Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso">HitTest(Point[], Single) Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
