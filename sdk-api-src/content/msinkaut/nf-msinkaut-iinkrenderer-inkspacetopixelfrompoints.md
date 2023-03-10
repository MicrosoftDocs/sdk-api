---
UID: NF:msinkaut.IInkRenderer.InkSpaceToPixelFromPoints
title: IInkRenderer::InkSpaceToPixelFromPoints (msinkaut.h)
description: Converts an array of points in ink space coordinates to an array of points in pixel space.
helpviewer_keywords: ["IInkRenderer interface [Tablet PC]","InkSpaceToPixelFromPoints method","IInkRenderer.InkSpaceToPixelFromPoints","IInkRenderer::InkSpaceToPixelFromPoints","InkSpaceToPixelFromPoints","InkSpaceToPixelFromPoints method [Tablet PC]","InkSpaceToPixelFromPoints method [Tablet PC]","IInkRenderer interface","e2b46752-fd9d-4e28-8f53-f16d7573ec89","msinkaut/IInkRenderer::InkSpaceToPixelFromPoints","tablet.inkrenderer_inkspacetopixelfrompoints"]
old-location: tablet\inkrenderer_inkspacetopixelfrompoints.htm
tech.root: tablet
ms.assetid: e2b46752-fd9d-4e28-8f53-f16d7573ec89
ms.date: 12/05/2018
ms.keywords: IInkRenderer interface [Tablet PC],InkSpaceToPixelFromPoints method, IInkRenderer.InkSpaceToPixelFromPoints, IInkRenderer::InkSpaceToPixelFromPoints, InkSpaceToPixelFromPoints, InkSpaceToPixelFromPoints method [Tablet PC], InkSpaceToPixelFromPoints method [Tablet PC],IInkRenderer interface, e2b46752-fd9d-4e28-8f53-f16d7573ec89, msinkaut/IInkRenderer::InkSpaceToPixelFromPoints, tablet.inkrenderer_inkspacetopixelfrompoints
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
 - IInkRenderer::InkSpaceToPixelFromPoints
 - msinkaut/IInkRenderer::InkSpaceToPixelFromPoints
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
 - IInkRenderer.InkSpaceToPixelFromPoints
---

# IInkRenderer::InkSpaceToPixelFromPoints


## -description

Converts an array of points in ink space coordinates to an array of points in pixel space.

## -parameters

### -param hDC [in]

The handle of the device context on which to draw.

### -param Points [in, out]

The array of points in ink space coordinates to convert into pixel locations. This should be an array of 32-bit integer values, passed within a VARIANT.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -returns

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

<b>InkSpaceToPixelFromPoints</b> applies the object transform, applies the view transform of the <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object, and then converts from inkspace to pixel units (1 ink unit = .01mm).

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel">InkSpaceToPixel Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace">PixelToInkSpace Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints">PixelToInkSpaceFromPoints Method</a>
