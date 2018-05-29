---
UID: NF:msinkaut.IInkStrokeDisp.NearestPoint
title: IInkStrokeDisp::NearestPoint
author: windows-sdk-content
description: Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates.
old-location: tablet\iinkstrokedisp_nearestpoint.htm
old-project: tablet
ms.assetid: 87c01f9d-b48a-459c-99f8-9634e1693fa0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: 87c01f9d-b48a-459c-99f8-9634e1693fa0, IInkStrokeDisp interface [Tablet PC],NearestPoint method, IInkStrokeDisp.NearestPoint, IInkStrokeDisp::NearestPoint, NearestPoint, NearestPoint method [Tablet PC], NearestPoint method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::NearestPoint, tablet.iinkstrokedisp_nearestpoint
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
-	IInkStrokeDisp.NearestPoint
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/fe042e12-21fa-4dae-988c-d082aa867520">GetRectangleIntersections Method</a>



<a href="https://msdn.microsoft.com/2025f728-cb08-4285-8584-c9ad537e58f2">HitTest(Point, Single) Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/e9ccf201-dbc9-484f-8038-6a964d304287">NearestPoint Method [InkDisp Class]</a>
 

 

