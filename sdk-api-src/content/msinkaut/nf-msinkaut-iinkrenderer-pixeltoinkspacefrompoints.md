---
UID: NF:msinkaut.IInkRenderer.PixelToInkSpaceFromPoints
title: IInkRenderer::PixelToInkSpaceFromPoints (msinkaut.h)
author: windows-sdk-content
description: Converts an array of locations in pixel space coordinates to an array of locations in ink space coordinates.
old-location: tablet\inkrenderer_pixeltoinkspacefrompoints.htm
tech.root: tablet
ms.assetid: 1427ab50-1b04-43a8-a987-838f2d6893cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1427ab50-1b04-43a8-a987-838f2d6893cc, IInkRenderer, IInkRenderer interface [Tablet PC],PixelToInkSpaceFromPoints method, IInkRenderer.PixelToInkSpaceFromPoints, IInkRenderer::PixelToInkSpaceFromPoints, PixelToInkSpaceFromPoints, PixelToInkSpaceFromPoints method [Tablet PC], PixelToInkSpaceFromPoints method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::PixelToInkSpaceFromPoints, tablet.inkrenderer_pixeltoinkspacefrompoints
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
 - IInkRenderer.PixelToInkSpaceFromPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRenderer::PixelToInkSpaceFromPoints


## -description



Converts an array of locations in pixel space coordinates to an array of locations in ink space  coordinates.




## -parameters




### -param hDC [in]

The handle of the device context for the containing control or form.


### -param Points [in, out]

The Variant array of points, as alternating Long x and y values of the form x0, y0, x1, y1, x2, y2, and so on, to convert from a pixel location to ink space coordinates.

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




<a href="https://msdn.microsoft.com/en-us/library/Mt846805(v=VS.85).aspx">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/9dfdc481-7129-47b1-9c5e-d17a70571ce2">InkSpaceToPixel Method</a>



<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints Method</a>



<a href="https://msdn.microsoft.com/fb881fe0-0be3-4e23-ac50-e421e2dc7845">PixelToInkSpace Method</a>
 

 

