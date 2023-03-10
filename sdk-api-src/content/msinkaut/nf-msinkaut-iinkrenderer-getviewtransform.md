---
UID: NF:msinkaut.IInkRenderer.GetViewTransform
title: IInkRenderer::GetViewTransform (msinkaut.h)
description: Gets the InkTransform object that represents the view transform that is used to render ink.
helpviewer_keywords: ["8a4d768d-09b6-45e1-b412-e267d92cc3ef","GetViewTransform","GetViewTransform method [Tablet PC]","GetViewTransform method [Tablet PC]","IInkRenderer interface","IInkRenderer interface [Tablet PC]","GetViewTransform method","IInkRenderer.GetViewTransform","IInkRenderer::GetViewTransform","msinkaut/IInkRenderer::GetViewTransform","tablet.inkrenderer_getviewtransform"]
old-location: tablet\inkrenderer_getviewtransform.htm
tech.root: tablet
ms.assetid: 8a4d768d-09b6-45e1-b412-e267d92cc3ef
ms.date: 12/05/2018
ms.keywords: 8a4d768d-09b6-45e1-b412-e267d92cc3ef, GetViewTransform, GetViewTransform method [Tablet PC], GetViewTransform method [Tablet PC],IInkRenderer interface, IInkRenderer interface [Tablet PC],GetViewTransform method, IInkRenderer.GetViewTransform, IInkRenderer::GetViewTransform, msinkaut/IInkRenderer::GetViewTransform, tablet.inkrenderer_getviewtransform
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
 - IInkRenderer::GetViewTransform
 - msinkaut/IInkRenderer::GetViewTransform
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
 - IInkRenderer.GetViewTransform
---

# IInkRenderer::GetViewTransform


## -description

Gets the <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the view transform that is used to render ink.

## -parameters

### -param ViewTransform [in]

 The matrix that represents the geometric transformation - rotation, scaling, shear, and reflection - values to use to transform the stroke coordinates within the ink space. The transformation applies to both the points and pen width. View transformation occurs after object transformation.

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
</table>

## -remarks

Any translations applied to this transform should be in ink space units (1 unit = .01mm).

Adjusting the view transform is analogous to adjusting the zoom factor on the ink rendering.

View transformation occurs after object transformation.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform">GetObjectTransform Method</a>



<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform">SetObjectTransform Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform">SetViewTransform Method</a>
