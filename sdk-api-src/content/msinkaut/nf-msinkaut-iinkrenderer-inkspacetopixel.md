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

# IInkRenderer::InkSpaceToPixel


## -description



Converts a location in ink space  coordinates to a location in pixel space using a handle for the conversion.




## -parameters




### -param hdcDisplay [in]

The handle of the device context.


### -param x [in, out]

The X-coordinate of the point to convert into a pixel location.


### -param y [in, out]

The Y-coordinate of the point to convert into a pixel location.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Coordinates overflowed during operation.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints</a> applies the object transform, applies the view transform of the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object, and then converts from inkspace to pixel units (1 ink unit = .01mm).




## -see-also




<a href="tablet.iinkrenderer">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints Method</a>



<a href="https://msdn.microsoft.com/fb881fe0-0be3-4e23-ac50-e421e2dc7845">PixelToInkSpace Method</a>



<a href="https://msdn.microsoft.com/1427ab50-1b04-43a8-a987-838f2d6893cc">PixelToInkSpaceFromPoints Method</a>
 

 

