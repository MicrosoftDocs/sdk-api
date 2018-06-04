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

# IInkRenderer::PixelToInkSpace


## -description



Converts a location in pixel space coordinates to be a location in ink space coordinates.




## -parameters




### -param hDC




### -param x [in, out]

The x coordinate of the point to convert into an ink location.


### -param y [in, out]

The y coordinate of the point to convert into an ink location.


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



<b>PixelToInkSpace</b> converts from pixel to ink space (1 HIMETRIC unit = .01mm), applies the inverse of the view transform, and then applies the object transform.




## -see-also




<a href="tablet.iinkrenderer">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/9dfdc481-7129-47b1-9c5e-d17a70571ce2">InkSpaceToPixel Method</a>



<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints Method</a>



<a href="https://msdn.microsoft.com/1427ab50-1b04-43a8-a987-838f2d6893cc">PixelToInkSpaceFromPoints Method</a>
 

 

