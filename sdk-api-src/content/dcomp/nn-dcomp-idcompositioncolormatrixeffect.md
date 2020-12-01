---
UID: NN:dcomp.IDCompositionColorMatrixEffect
title: IDCompositionColorMatrixEffect (dcomp.h)
description: The color matrix effect alters the RGBA values of a bitmap.
helpviewer_keywords: ["IDCompositionColorMatrixEffect","IDCompositionColorMatrixEffect interface [DirectComposition]","IDCompositionColorMatrixEffect interface [DirectComposition]","described","dcomp/IDCompositionColorMatrixEffect","directcomp.idcompositioncolormatrixeffect"]
old-location: directcomp\idcompositioncolormatrixeffect.htm
tech.root: directcomp
ms.assetid: 75528E11-D041-4192-833A-31679316DF76
ms.date: 12/05/2018
ms.keywords: IDCompositionColorMatrixEffect, IDCompositionColorMatrixEffect interface [DirectComposition], IDCompositionColorMatrixEffect interface [DirectComposition],described, dcomp/IDCompositionColorMatrixEffect, directcomp.idcompositioncolormatrixeffect
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
 - IDCompositionColorMatrixEffect
 - dcomp/IDCompositionColorMatrixEffect
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
 - IDCompositionColorMatrixEffect
---

# IDCompositionColorMatrixEffect interface


## -description

The color matrix effect alters the RGBA values of a bitmap.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionColorMatrixEffect</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionColorMatrixEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionColorMatrixEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioncolormatrixeffect-setalphamode">SetAlphaMode</a>
</td>
<td align="left" width="63%">
Sets the alpha mode of the output for the color matrix effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioncolormatrixeffect-setclampoutput">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioncolormatrixeffect-setmatrix">SetMatrix</a>
</td>
<td align="left" width="63%">
Sets the matrix used by the effect to multiply the RGBA values of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-setmatrixelement">SetMatrixElement</a>
</td>
<td align="left" width="63%">Overloaded. Sets an element of the color matrix.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>