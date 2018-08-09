---
UID: NF:msinkaut.IInkDisp.HitTestCircle
title: IInkDisp::HitTestCircle
author: windows-sdk-content
description: Retrieves the InkStrokes collection that are either completely inside or intersected by a known circle.
old-location: tablet\inkdisp_hittest_point__single.htm
old-project: tablet
ms.assetid: 2025f728-cb08-4285-8584-c9ad537e58f2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 2025f728-cb08-4285-8584-c9ad537e58f2, HitTestCircle, HitTestCircle method [Tablet PC], HitTestCircle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],HitTestCircle method, IInkDisp.HitTestCircle, IInkDisp::HitTestCircle, msinkaut/IInkDisp::HitTestCircle, tablet.inkdisp_hittest_point__single
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDisp::HitTestCircle


## -description


Retrieves the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that are either completely inside or intersected by a known circle.
        


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

To determine which points of a known stroke intersect the test area, call the <a href="https://msdn.microsoft.com/b87a1bc0-b17b-419b-947e-48746f4903e8">HitTest</a> method of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object.

The application must always pass in a destination pointer for the resulting collection of strokes. If there are no intersections, the collection has a count of zero.




## -see-also




<a href="https://msdn.microsoft.com/fe88410d-e3e7-4899-b6fe-04e6eed98bbb">HitTest(Point[], Single) Method</a>



<a href="https://msdn.microsoft.com/401c4f62-a406-49ac-9911-91f815cde9c8">HitTest(Rectangle, Single) Method</a>



<a href="tablet.iinkdisp">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

