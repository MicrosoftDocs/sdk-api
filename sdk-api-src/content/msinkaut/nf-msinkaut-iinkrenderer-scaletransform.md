---
UID: NF:msinkaut.IInkRenderer.ScaleTransform
title: IInkRenderer::ScaleTransform (msinkaut.h)
description: Scales the view transform in the X and Y dimension.
helpviewer_keywords: ["63a7d5f7-2c93-4f45-ad8d-aa3f75f78eff","IInkRenderer interface [Tablet PC]","ScaleTransform method","IInkRenderer.ScaleTransform","IInkRenderer::ScaleTransform","ScaleTransform","ScaleTransform method [Tablet PC]","ScaleTransform method [Tablet PC]","IInkRenderer interface","msinkaut/IInkRenderer::ScaleTransform","tablet.inkrenderer_scaletransform"]
old-location: tablet\inkrenderer_scaletransform.htm
tech.root: tablet
ms.assetid: 63a7d5f7-2c93-4f45-ad8d-aa3f75f78eff
ms.date: 12/05/2018
ms.keywords: 63a7d5f7-2c93-4f45-ad8d-aa3f75f78eff, IInkRenderer interface [Tablet PC],ScaleTransform method, IInkRenderer.ScaleTransform, IInkRenderer::ScaleTransform, ScaleTransform, ScaleTransform method [Tablet PC], ScaleTransform method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::ScaleTransform, tablet.inkrenderer_scaletransform
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
 - IInkRenderer::ScaleTransform
 - msinkaut/IInkRenderer::ScaleTransform
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
 - IInkRenderer.ScaleTransform
---

# IInkRenderer::ScaleTransform


## -description

Scales the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">view transform</a> in the X and Y dimension.

## -parameters

### -param HorizontalMultiplier [in]

The factor to scale the X dimension in the view transform.

### -param VerticalMultiplier [in]

The factor to scale the Y dimension in the view transform.

### -param ApplyOnPenWidth [in, optional]

Optional. <b>VARIANT_TRUE</b> to apply the scale factors to the pen width; otherwise, <b>VARIANT_FALSE</b>. The default is <b>VARIANT_TRUE</b>.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>
