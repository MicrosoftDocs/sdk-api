---
UID: NF:msinkaut.IInkDisp.HitTestWithLasso
title: IInkDisp::HitTestWithLasso (msinkaut.h)
description: Retrieves the strokes within a polyline selection area.
helpviewer_keywords: ["HitTestWithLasso","HitTestWithLasso method [Tablet PC]","HitTestWithLasso method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","HitTestWithLasso method","IInkDisp.HitTestWithLasso","IInkDisp::HitTestWithLasso","fe88410d-e3e7-4899-b6fe-04e6eed98bbb","msinkaut/IInkDisp::HitTestWithLasso","tablet.inkdisp_hittest_point____single"]
old-location: tablet\inkdisp_hittest_point____single.htm
tech.root: tablet
ms.assetid: fe88410d-e3e7-4899-b6fe-04e6eed98bbb
ms.date: 12/05/2018
ms.keywords: HitTestWithLasso, HitTestWithLasso method [Tablet PC], HitTestWithLasso method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],HitTestWithLasso method, IInkDisp.HitTestWithLasso, IInkDisp::HitTestWithLasso, fe88410d-e3e7-4899-b6fe-04e6eed98bbb, msinkaut/IInkDisp::HitTestWithLasso, tablet.inkdisp_hittest_point____single
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
 - IInkDisp::HitTestWithLasso
 - msinkaut/IInkDisp::HitTestWithLasso
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
 - IInkDisp.HitTestWithLasso
---

# IInkDisp::HitTestWithLasso


## -description

Retrieves the strokes within a polyline selection area.

## -parameters

### -param Points [in]

The points that are used in the selection tool to select the strokes. The selection area is the area inside the selection boundary in which the boundary first intersects itself. If the boundary does not intersect itself, the method adds a point to the end of the array to create a straight line from the first point to the last point. If the boundary is a straight line (no area within the selection boundary), no strokes are selected.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param IntersectPercent [in]

The percentage of stroke points that must be contained within the selection tool to include the stroke in the resulting collection of strokes. If zero (<code>0</code>), all strokes that are contained within or intersected by the selection tool are included in the resulting collection of strokes. If 100, only strokes fully contained in the selection tool are included in the collection. Strokes that intersect the selection tool are included in the collection if the percentage of points in those strokes contained within the selection tool is greater than or equal to the <i>percentIntersect</i> percentage. Fractional percentages are rounded up.

### -param LassoPoints [in, out, optional]

Optional. Retrieves the specific portion of the selection tool that is used for the selection. Because a user can draw many different types of selection tools, some of which overlap multiple times, this can be useful for illustrating which portion of the selection tool was used for selection. The default value is a <b>NULL</b> pointer, which means no information is returned.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle">HitTest(Point, Single) Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle">HitTest(Rectangle, Single) Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
