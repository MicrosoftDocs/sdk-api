---
UID: NF:msinkaut.IInkStrokeDisp.HitTestCircle
title: IInkStrokeDisp::HitTestCircle (msinkaut.h)
description: Determines whether a stroke is either completely inside or intersected by a given circle.
helpviewer_keywords: ["HitTestCircle","HitTestCircle method [Tablet PC]","HitTestCircle method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","HitTestCircle method","IInkStrokeDisp.HitTestCircle","IInkStrokeDisp::HitTestCircle","b87a1bc0-b17b-419b-947e-48746f4903e8","msinkaut/IInkStrokeDisp::HitTestCircle","tablet.iinkstrokedisp_hittestcircle"]
old-location: tablet\iinkstrokedisp_hittestcircle.htm
tech.root: tablet
ms.assetid: b87a1bc0-b17b-419b-947e-48746f4903e8
ms.date: 12/05/2018
ms.keywords: HitTestCircle, HitTestCircle method [Tablet PC], HitTestCircle method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],HitTestCircle method, IInkStrokeDisp.HitTestCircle, IInkStrokeDisp::HitTestCircle, b87a1bc0-b17b-419b-947e-48746f4903e8, msinkaut/IInkStrokeDisp::HitTestCircle, tablet.iinkstrokedisp_hittestcircle
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
 - IInkStrokeDisp::HitTestCircle
 - msinkaut/IInkStrokeDisp::HitTestCircle
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
 - IInkStrokeDisp.HitTestCircle
---

# IInkStrokeDisp::HitTestCircle


## -description

Determines whether a stroke is either completely inside or intersected by a given circle.

## -parameters

### -param X [in]

The x-position of the center of the hit-test circle in ink space coordinates.

### -param Y [in]

The y-position of the center of the hit-test circle in ink space coordinates.

### -param Radius [in]

The radius of the circle to use in the hit test.

### -param Intersects [out, retval]

<b>VARIANT_TRUE</b> if the stroke intersects or is inside the circle; otherwise, <b>VARIANT_FALSE</b>

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
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getrectangleintersections">GetRectangleIntersections Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle">HitTest(Point, Single) Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-nearestpoint">NearestPoint Method [IInkStrokeDisp Interface]</a>