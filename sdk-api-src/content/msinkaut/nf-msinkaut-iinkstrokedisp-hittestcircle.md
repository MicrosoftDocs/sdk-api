---
UID: NF:msinkaut.IInkStrokeDisp.HitTestCircle
title: IInkStrokeDisp::HitTestCircle
author: windows-sdk-content
description: Determines whether a stroke is either completely inside or intersected by a given circle.
old-location: tablet\iinkstrokedisp_hittestcircle.htm
old-project: tablet
ms.assetid: b87a1bc0-b17b-419b-947e-48746f4903e8
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: HitTestCircle, HitTestCircle method [Tablet PC], HitTestCircle method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],HitTestCircle method, IInkStrokeDisp.HitTestCircle, IInkStrokeDisp::HitTestCircle, b87a1bc0-b17b-419b-947e-48746f4903e8, msinkaut/IInkStrokeDisp::HitTestCircle, tablet.iinkstrokedisp_hittestcircle
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
 - IInkStrokeDisp.HitTestCircle
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/fe042e12-21fa-4dae-988c-d082aa867520">GetRectangleIntersections Method</a>



<a href="https://msdn.microsoft.com/2025f728-cb08-4285-8584-c9ad537e58f2">HitTest(Point, Single) Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/87c01f9d-b48a-459c-99f8-9634e1693fa0">NearestPoint Method [IInkStrokeDisp Interface]</a>
 

 

