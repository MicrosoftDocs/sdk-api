---
UID: NF:msinkaut.IInkRenderer.PixelToInkSpaceFromPoints
title: IInkRenderer::PixelToInkSpaceFromPoints (msinkaut.h)
description: Converts an array of locations in pixel space coordinates to an array of locations in ink space coordinates.
helpviewer_keywords: ["1427ab50-1b04-43a8-a987-838f2d6893cc","IInkRenderer","IInkRenderer interface [Tablet PC]","PixelToInkSpaceFromPoints method","IInkRenderer.PixelToInkSpaceFromPoints","IInkRenderer::PixelToInkSpaceFromPoints","PixelToInkSpaceFromPoints","PixelToInkSpaceFromPoints method [Tablet PC]","PixelToInkSpaceFromPoints method [Tablet PC]","IInkRenderer interface","msinkaut/IInkRenderer::PixelToInkSpaceFromPoints","tablet.inkrenderer_pixeltoinkspacefrompoints"]
old-location: tablet\inkrenderer_pixeltoinkspacefrompoints.htm
tech.root: tablet
ms.assetid: 1427ab50-1b04-43a8-a987-838f2d6893cc
ms.date: 12/05/2018
ms.keywords: 1427ab50-1b04-43a8-a987-838f2d6893cc, IInkRenderer, IInkRenderer interface [Tablet PC],PixelToInkSpaceFromPoints method, IInkRenderer.PixelToInkSpaceFromPoints, IInkRenderer::PixelToInkSpaceFromPoints, PixelToInkSpaceFromPoints, PixelToInkSpaceFromPoints method [Tablet PC], PixelToInkSpaceFromPoints method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::PixelToInkSpaceFromPoints, tablet.inkrenderer_pixeltoinkspacefrompoints
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRenderer::PixelToInkSpaceFromPoints
 - msinkaut/IInkRenderer::PixelToInkSpaceFromPoints
dev_langs:
 - c++
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
---

# IInkRenderer::PixelToInkSpaceFromPoints


## -description

Converts an array of locations in pixel space coordinates to an array of locations in ink space  coordinates.

## -parameters

### -param hDC [in]

The handle of the device context for the containing control or form.

### -param Points [in, out]

The Variant array of points, as alternating Long x and y values of the form x0, y0, x1, y1, x2, y2, and so on, to convert from a pixel location to ink space coordinates.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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

<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel">InkSpaceToPixel Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints">InkSpaceToPixelFromPoints Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace">PixelToInkSpace Method</a>
