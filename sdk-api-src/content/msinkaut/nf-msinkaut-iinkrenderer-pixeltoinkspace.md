---
UID: NF:msinkaut.IInkRenderer.PixelToInkSpace
title: IInkRenderer::PixelToInkSpace (msinkaut.h)
description: Converts a location in pixel space coordinates to be a location in ink space coordinates.
helpviewer_keywords: ["IInkRenderer interface [Tablet PC]","PixelToInkSpace method","IInkRenderer.PixelToInkSpace","IInkRenderer::PixelToInkSpace","PixelToInkSpace","PixelToInkSpace method [Tablet PC]","PixelToInkSpace method [Tablet PC]","IInkRenderer interface","fb881fe0-0be3-4e23-ac50-e421e2dc7845","msinkaut/IInkRenderer::PixelToInkSpace","tablet.inkrenderer_pixeltoinkspace"]
old-location: tablet\inkrenderer_pixeltoinkspace.htm
tech.root: tablet
ms.assetid: fb881fe0-0be3-4e23-ac50-e421e2dc7845
ms.date: 12/05/2018
ms.keywords: IInkRenderer interface [Tablet PC],PixelToInkSpace method, IInkRenderer.PixelToInkSpace, IInkRenderer::PixelToInkSpace, PixelToInkSpace, PixelToInkSpace method [Tablet PC], PixelToInkSpace method [Tablet PC],IInkRenderer interface, fb881fe0-0be3-4e23-ac50-e421e2dc7845, msinkaut/IInkRenderer::PixelToInkSpace, tablet.inkrenderer_pixeltoinkspace
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
 - IInkRenderer::PixelToInkSpace
 - msinkaut/IInkRenderer::PixelToInkSpace
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
 - IInkRenderer.PixelToInkSpace
---

# IInkRenderer::PixelToInkSpace


## -description

Converts a location in pixel space coordinates to be a location in ink space coordinates.

## -parameters

### -param hDC [in]

The handle of the device context for the containing control or form.

### -param x [in, out]

The x coordinate of the point to convert into an ink location.

### -param y [in, out]

The y coordinate of the point to convert into an ink location.

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

<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel">InkSpaceToPixel Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints">InkSpaceToPixelFromPoints Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints">PixelToInkSpaceFromPoints Method</a>
