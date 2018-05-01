---
UID: NF:msinkaut.IInkStrokeDisp.GetRectangleIntersections
title: IInkStrokeDisp::GetRectangleIntersections method
author: windows-driver-content
description: Finds the points where a IInkStrokeDisp object intersects a given rectangle.
old-location: tablet\iinkstrokedisp_getrectangleintersections.htm
old-project: tablet
ms.assetid: fe042e12-21fa-4dae-988c-d082aa867520
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetRectangleIntersections method [Tablet PC], GetRectangleIntersections method [Tablet PC], IInkStrokeDisp interface, GetRectangleIntersections,IInkStrokeDisp.GetRectangleIntersections, IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], GetRectangleIntersections method, IInkStrokeDisp::GetRectangleIntersections, fe042e12-21fa-4dae-988c-d082aa867520, msinkaut/IInkStrokeDisp::GetRectangleIntersections, tablet.iinkstrokedisp_getrectangleintersections
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.GetRectangleIntersections
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkStrokeDisp::GetRectangleIntersections method


## -description



Finds the points where a <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object intersects a given rectangle.




## -parameters




### -param Rectangle [in]

The rectangle in <b>ink space</b> coordinates, that describes the hit test area.


### -param Intersections [out, retval]

When this method returns, contains a VARIANT array that indicates where the stroke intersects the <i>rectangle</i>. The beginning floating point indices are stored in the even indices. The ending floating point indices are stored in the odd indices. The first pair of indices represents the first intersection.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
Cannot allocate Stroke handler helper object.

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
</table>
 




## -remarks



This method returns an array that indicates where the stroke intersects the specified rectangle. Each segment of the stroke that intersects the rectangle is one pair of indices, alternating with a beginning index followed by an ending index.

If the stroke begins within the test rectangle, the first index is set to -1. If the stroke ends within the test rectangle, the last index is set to -1. If the stroke is wholly outside the test rectangle, an empty array is returned. For example, if a stroke begins inside the test rectangle, leaves the boundaries of the rectangle, returns inside, and leaves again, then the <b>GetRectangleIntersections</b> method might return {-1, 1.4, 5.5, 10.1} to describe the two segments of the stroke falling within the rectangle.




## -see-also




<a href="https://msdn.microsoft.com/d3733613-fc8e-41f2-9172-07b61fc133dd">Clip Method</a>



<a href="https://msdn.microsoft.com/a070fc87-608c-47be-b9b2-e2a41a31226f">FindIntersections Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

