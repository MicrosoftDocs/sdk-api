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

# IDirectManipulationPrimaryContent::SetSnapInterval


## -description


    Specifies snap points for the inertia end position at uniform intervals.


## -parameters




### -param motion [in]

One of the <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values.


### -param interval [in]

The interval between each snap point.


### -param offset [in]

The offset from the coordinate specified in <a href="https://msdn.microsoft.com/3f9afe1b-20f4-45fa-a63b-25b7a0c597af">SetSnapCoordinate</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Snap point locations are in content coordinate units. 

Specify snap points through <a href="https://msdn.microsoft.com/3257952d-903b-455c-9422-9739411a5924">SetSnapPoints</a> or <b>SetSnapInterval</b>. 

If snap points are invalid (for example, outside of the content boundaries), they are ignored and the content is always within the content boundaries. 

Snap points are not at boundaries by default. If you wish for content to stop at a boundary, a snap point must be set at the boundary.

 Snap points set by <b>SetSnapInterval</b> can be cleared by calling <b>SetSnapInterval</b> with an interval of 0.0f.


#### Examples

The following example shows how to set the coordinate system for X translation snap points to the origin. Snap points are set every 45 pixels, beginning at the origin along the X-axis.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr = SetSnapCoordinate(testWindow, 0, DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_ORIGIN, 0.0f);
hr = pContent-&gt;SetSnapInterval(DIRECTMANIPULATION_MOTION_TRANSLATEX, 45.0f, 0.0f);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>



<a href="https://msdn.microsoft.com/3f9afe1b-20f4-45fa-a63b-25b7a0c597af">SetSnapCoordinate</a>



<a href="https://msdn.microsoft.com/3257952d-903b-455c-9422-9739411a5924">SetSnapPoints</a>
 

 

