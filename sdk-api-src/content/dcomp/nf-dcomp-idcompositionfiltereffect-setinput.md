---
UID: NF:dcomp.IDCompositionFilterEffect.SetInput
title: IDCompositionFilterEffect::SetInput (dcomp.h)
description: Sets the input at an index to the specified filter effect.
helpviewer_keywords: ["IDCompositionFilterEffect interface [DirectComposition]","SetInput method","IDCompositionFilterEffect.SetInput","IDCompositionFilterEffect::SetInput","SetInput","SetInput method [DirectComposition]","SetInput method [DirectComposition]","IDCompositionFilterEffect interface","dcomp/IDCompositionFilterEffect::SetInput","directcomp.idcompositionfiltereffect_setinput"]
old-location: directcomp\idcompositionfiltereffect_setinput.htm
tech.root: directcomp
ms.assetid: 8DFF137E-2979-42D4-A8A5-F831A33468CA
ms.date: 12/05/2018
ms.keywords: IDCompositionFilterEffect interface [DirectComposition],SetInput method, IDCompositionFilterEffect.SetInput, IDCompositionFilterEffect::SetInput, SetInput, SetInput method [DirectComposition], SetInput method [DirectComposition],IDCompositionFilterEffect interface, dcomp/IDCompositionFilterEffect::SetInput, directcomp.idcompositionfiltereffect_setinput
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
 - IDCompositionFilterEffect::SetInput
 - dcomp/IDCompositionFilterEffect::SetInput
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
 - IDCompositionFilterEffect.SetInput
---

# IDCompositionFilterEffect::SetInput


## -description

Sets the input at an index to the specified filter effect.

## -parameters

### -param index [in]

Type: <b>UINT</b>

Specifies the index the to apply the filter effect at.

### -param input [in, optional]

Type: <b>IUnknown*</b>

The filter effect to apply.
          The following effects are available:
          

<ul>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionaffinetransform2deffect">IDCompositionAffineTransform2DEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionblendeffect">IDCompositionBlendEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncompositeeffect">IDCompositionCompositeEffect</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/dn919732(v=vs.85)">IDCompositionFloodEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionhuerotationeffect">IDCompositionHueRotationEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>
</li>
<li>
<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>
</li>
</ul>

### -param flags [in]

Type: <b>UINT</b>

Flags to apply to the filter effect.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
