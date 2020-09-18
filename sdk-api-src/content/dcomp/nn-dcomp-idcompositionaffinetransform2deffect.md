---
UID: NN:dcomp.IDCompositionAffineTransform2DEffect
title: IDCompositionAffineTransform2DEffect (dcomp.h)
description: The arithmetic composite effect is used to combine 2 images using a weighted sum of pixels from the input images.
helpviewer_keywords: ["IDCompositionAffineTransform2DEffect","IDCompositionAffineTransform2DEffect interface [DirectComposition]","IDCompositionAffineTransform2DEffect interface [DirectComposition]","described","dcomp/IDCompositionAffineTransform2DEffect","directcomp.idcompositionaffinetransform2deffect"]
old-location: directcomp\idcompositionaffinetransform2deffect.htm
tech.root: directcomp
ms.assetid: 1B693705-1118-4B9B-A7B7-E8811AE881AC
ms.date: 12/05/2018
ms.keywords: IDCompositionAffineTransform2DEffect, IDCompositionAffineTransform2DEffect interface [DirectComposition], IDCompositionAffineTransform2DEffect interface [DirectComposition],described, dcomp/IDCompositionAffineTransform2DEffect, directcomp.idcompositionaffinetransform2deffect
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionAffineTransform2DEffect
 - dcomp/IDCompositionAffineTransform2DEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionAffineTransform2DEffect
---

# IDCompositionAffineTransform2DEffect interface


## -description

The arithmetic composite effect is used to combine 2 images using a weighted sum of pixels from the input images.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionAffineTransform2DEffect</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionAffineTransform2DEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionAffineTransform2DEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionaffinetransform2deffect-setbordermode">SetBorderMode</a>
</td>
<td align="left" width="63%">
Sets the border mode to use with the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionaffinetransform2deffect-setinterpolationmode">SetInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the interpolation mode of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/directcomp/idcompositionaffinetransform2deffect-setsharpness-overloaded">SetSharpness</a>
</td>
<td align="left" width="63%">Overloaded. Sets the sharpness of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionaffinetransform2deffect-settransformmatrix">SetTransformMatrix</a>
</td>
<td align="left" width="63%">
Sets the transform matrix of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-settransformmatrixelement">settransformmatrixelement</a>
</td>
<td align="left" width="63%">Overloaded. Sets an element of the transform matrix of the effect.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>