---
UID: NF:msinkaut.IInkDisp.HitTestWithRectangle
title: IInkDisp::HitTestWithRectangle
author: windows-sdk-content
description: Retrieves the strokes that are contained within a specified rectangle.
old-location: tablet\inkdisp_hittest_rectangle__single.htm
old-project: tablet
ms.assetid: 401c4f62-a406-49ac-9911-91f815cde9c8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 401c4f62-a406-49ac-9911-91f815cde9c8, HitTestWithRectangle, HitTestWithRectangle method [Tablet PC], HitTestWithRectangle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],HitTestWithRectangle method, IInkDisp.HitTestWithRectangle, IInkDisp::HitTestWithRectangle, msinkaut/IInkDisp::HitTestWithRectangle, tablet.inkdisp_hittest_rectangle__single
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
 - IInkDisp.HitTestWithRectangle
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDisp::HitTestWithRectangle


## -description


Retrieves the strokes that are contained within a specified rectangle.


## -parameters




### -param SelectionRectangle [in]

The selection rectangle, of type <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a>, in ink space coordinates.


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



To determine which points of a known stroke intersect the test area, call the <a href="https://msdn.microsoft.com/fe042e12-21fa-4dae-988c-d082aa867520">GetRectangleIntersections</a> method of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object, which retrieves the points where a stroke intersects a known rectangle.




## -see-also




<a href="https://msdn.microsoft.com/2025f728-cb08-4285-8584-c9ad537e58f2">HitTest(Point, Single) Method</a>



<a href="https://msdn.microsoft.com/fe88410d-e3e7-4899-b6fe-04e6eed98bbb">HitTest(Point[], Single) Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846797(v=VS.85).aspx">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

