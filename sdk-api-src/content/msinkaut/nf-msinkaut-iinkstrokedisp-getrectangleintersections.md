---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkStrokeDisp::GetRectangleIntersections


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
 

 

