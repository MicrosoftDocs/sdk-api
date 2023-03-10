---
UID: NF:msinkaut.IInkStrokeDisp.GetBoundingBox
title: IInkStrokeDisp::GetBoundingBox (msinkaut.h)
description: Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or an InkStrokes collection. (IInkStrokeDisp.GetBoundingBox)
helpviewer_keywords: ["3b2c8cfc-05e6-4b53-b709-72291ee78471","GetBoundingBox","GetBoundingBox method [Tablet PC]","GetBoundingBox method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","GetBoundingBox method","IInkStrokeDisp.GetBoundingBox","IInkStrokeDisp::GetBoundingBox","msinkaut/IInkStrokeDisp::GetBoundingBox","tablet.iinkstrokedisp_getboundingbox"]
old-location: tablet\iinkstrokedisp_getboundingbox.htm
tech.root: tablet
ms.assetid: 3b2c8cfc-05e6-4b53-b709-72291ee78471
ms.date: 12/05/2018
ms.keywords: 3b2c8cfc-05e6-4b53-b709-72291ee78471, GetBoundingBox, GetBoundingBox method [Tablet PC], GetBoundingBox method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetBoundingBox method, IInkStrokeDisp.GetBoundingBox, IInkStrokeDisp::GetBoundingBox, msinkaut/IInkStrokeDisp::GetBoundingBox, tablet.iinkstrokedisp_getboundingbox
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
 - IInkStrokeDisp::GetBoundingBox
 - msinkaut/IInkStrokeDisp::GetBoundingBox
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
 - IInkStrokeDisp.GetBoundingBox
---

# IInkStrokeDisp::GetBoundingBox


## -description

Retrieves the bounding box in <b>ink space</b> coordinates for either all of the strokes in an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, an individual stroke, or an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param BoundingBoxMode [in, optional]

Optional. Specifies the stroke characteristics to use to calculate the bounding box. The default value is -1, indicating that all characteristics of a stroke are used to specify the bounding box. 

For more details about the use of stroke characteristics to calculate a bounding box, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkboundingboxmode">BoundingBoxMode</a> enumeration type.

### -param Rectangle [out, retval]

When this method returns, contains a pointer to the rectangle that defines the bounding box of an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object, or an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

<div class="alert"><b>Note</b>  For an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object, the returned bounding box is a copy of the strokes bounding box, so altering the returned bounding box does not affect the strokes location.</div>
<div> </div>

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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object is not registered.

</td>
</tr>
</table>

## -remarks

When the bounding box is affected by the pen width, then this width is scaled appropriately for the <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a>'s view transform. To do this, the pen width is multiplied by the square root of the determinant of the view transform.

<div class="alert"><b>Note</b>  In Windows Vista and later versions, <b>GetBoundingBox Method</b> does not take the width of the stroke into account.</div>
<div> </div>
<div class="alert"><b>Note</b>  If you have not set the pen width explicitly, it is 53 by default. You must multiply the pen width by the square root of the determinant to yield the correct bounding box. The height and width of the bounding box are expanded by half this amount in each direction. For example, consider that the pen width is 53, the square root of the determinant is 50, and the bounding box is (0, 0, 1000, 1000). The pen width adjustment to the bounding box in each direction is calculated as (53 * 50) / 2, and the right and bottom sides are incremented by one. This results in a rendered bounding box of (-1325, -1325, 2326, 2326).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkboundingboxmode">InkBoundingBoxMode Enumeration</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>
