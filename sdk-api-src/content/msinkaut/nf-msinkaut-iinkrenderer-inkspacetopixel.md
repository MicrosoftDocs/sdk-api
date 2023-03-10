---
UID: NF:msinkaut.IInkRenderer.InkSpaceToPixel
title: IInkRenderer::InkSpaceToPixel (msinkaut.h)
description: Converts a location in ink space coordinates to a location in pixel space using a handle for the conversion.
helpviewer_keywords: ["9dfdc481-7129-47b1-9c5e-d17a70571ce2","IInkRenderer","IInkRenderer interface [Tablet PC]","InkSpaceToPixel method","IInkRenderer.InkSpaceToPixel","IInkRenderer::InkSpaceToPixel","InkSpaceToPixel","InkSpaceToPixel method [Tablet PC]","InkSpaceToPixel method [Tablet PC]","IInkRenderer interface","msinkaut/IInkRenderer::InkSpaceToPixel","tablet.inkrenderer_inkspacetopixel"]
old-location: tablet\inkrenderer_inkspacetopixel.htm
tech.root: tablet
ms.assetid: 9dfdc481-7129-47b1-9c5e-d17a70571ce2
ms.date: 12/05/2018
ms.keywords: 9dfdc481-7129-47b1-9c5e-d17a70571ce2, IInkRenderer, IInkRenderer interface [Tablet PC],InkSpaceToPixel method, IInkRenderer.InkSpaceToPixel, IInkRenderer::InkSpaceToPixel, InkSpaceToPixel, InkSpaceToPixel method [Tablet PC], InkSpaceToPixel method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::InkSpaceToPixel, tablet.inkrenderer_inkspacetopixel
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
 - IInkRenderer::InkSpaceToPixel
 - msinkaut/IInkRenderer::InkSpaceToPixel
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
 - IInkRenderer.InkSpaceToPixel
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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints">InkSpaceToPixelFromPoints</a> applies the object transform, applies the view transform of the <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object, and then converts from inkspace to pixel units (1 ink unit = .01mm).

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints">InkSpaceToPixelFromPoints Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace">PixelToInkSpace Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints">PixelToInkSpaceFromPoints Method</a>
