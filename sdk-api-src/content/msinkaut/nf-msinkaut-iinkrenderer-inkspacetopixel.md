---
UID: NF:msinkaut.IInkRenderer.InkSpaceToPixel
title: IInkRenderer::InkSpaceToPixel
author: windows-sdk-content
description: Converts a location in ink space coordinates to a location in pixel space using a handle for the conversion.
old-location: tablet\inkrenderer_inkspacetopixel.htm
tech.root: tablet
ms.assetid: 9dfdc481-7129-47b1-9c5e-d17a70571ce2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 9dfdc481-7129-47b1-9c5e-d17a70571ce2, IInkRenderer, IInkRenderer interface [Tablet PC],InkSpaceToPixel method, IInkRenderer.InkSpaceToPixel, IInkRenderer::InkSpaceToPixel, InkSpaceToPixel, InkSpaceToPixel method [Tablet PC], InkSpaceToPixel method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::InkSpaceToPixel, tablet.inkrenderer_inkspacetopixel
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRenderer.InkSpaceToPixel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/2AB56616-3F67-4428-8A99-FCE733A5FDBF">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints Method</a>



<a href="https://msdn.microsoft.com/fb881fe0-0be3-4e23-ac50-e421e2dc7845">PixelToInkSpace Method</a>



<a href="https://msdn.microsoft.com/1427ab50-1b04-43a8-a987-838f2d6893cc">PixelToInkSpaceFromPoints Method</a>
 

 

