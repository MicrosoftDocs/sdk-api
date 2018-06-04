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

# IViewObjectEx::GetRect


## -description


Retrieves a rectangle describing a requested drawing aspect.


## -parameters




### -param dwAspect [in]

The drawing aspect requested.


### -param pRect [out]

A pointer to the rectangle describing the requested drawing aspect.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
The method does not support the specified aspect. Either the object does not support the aspect requested or the aspect is not rectangular.

</td>
</tr>
</table>
 




## -remarks



This method returns a rectangle describing the specified drawing aspect. The returned rectangle is in <b>HIMETRIC</b> units, relative to the object's origin. The rectangle returned depends on the drawing aspect as follows.

<table>
<tr>
<th>Drawing Aspect</th>
<th>Description</th>
</tr>
<tr>
<td>
DVASPECT_CONTENT

</td>
<td>
Objects should return the bounding rectangle of the whole object. The top-left corner is at the object's origin and the size is equal to the extent returned by <a href="https://msdn.microsoft.com/66eedee0-58b5-4676-93db-599ed19a02b6">IViewObject2::GetExtent</a>.

</td>
</tr>
<tr>
<td>
DVASPECT_OPAQUE

</td>
<td>
Objects with a rectangular opaque region should return that rectangle. Others should fail and return error code DV_E_DVASPECT.

If a rectangle is returned, it is guaranteed to be completely obscured by calling <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> for that aspect. The container should use that rectangle to clip out the object's opaque parts before drawing any object behind it during the back to front pass. If this method fails on an object with a non-rectangular opaque region, the container should draw the entire object in the back to front part using the DVASPECT_CONTENT aspect.

</td>
</tr>
<tr>
<td>
DVASPECT_TRANSPARENT

</td>
<td>
Objects should return the rectangle covering all transparent or irregular parts. If the object does not have any transparent or irregular parts, it may return DV_E_ASPECT. A container may use this rectangle to determine whether there are other objects overlapping the transparent parts of a given object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a>
 

 

