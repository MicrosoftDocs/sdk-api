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

# IInkRenderer::PixelToInkSpaceFromPoints


## -description



Converts an array of locations in pixel space coordinates to an array of locations in ink space  coordinates.




## -parameters




### -param hDC




### -param Points [in, out]

The Variant array of points, as alternating Long x and y values of the form x0, y0, x1, y1, x2, y2, and so on, to convert from a pixel location to ink space coordinates.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


#### - hdcDisplay [in]

The handle of the device context for the containing control or form.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



<code>PixelToInkSpaceFromPoints</code> converts from pixel to ink space (1 ink unit = .01mm), applies the inverse of the view transform, and then applies the inverse of the object transform.




## -see-also




<a href="tablet.iinkrenderer">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/9dfdc481-7129-47b1-9c5e-d17a70571ce2">InkSpaceToPixel Method</a>



<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints Method</a>



<a href="https://msdn.microsoft.com/fb881fe0-0be3-4e23-ac50-e421e2dc7845">PixelToInkSpace Method</a>
 

 

