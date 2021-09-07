---
UID: NF:dcomp.IDCompositionAffineTransform2DEffect.SetInterpolationMode
title: IDCompositionAffineTransform2DEffect::SetInterpolationMode (dcomp.h)
description: Sets the interpolation mode of the effect.
helpviewer_keywords: ["IDCompositionAffineTransform2DEffect interface [DirectComposition]","SetInterpolationMode method","IDCompositionAffineTransform2DEffect.SetInterpolationMode","IDCompositionAffineTransform2DEffect::SetInterpolationMode","SetInterpolationMode","SetInterpolationMode method [DirectComposition]","SetInterpolationMode method [DirectComposition]","IDCompositionAffineTransform2DEffect interface","dcomp/IDCompositionAffineTransform2DEffect::SetInterpolationMode","directcomp.idcompositionaffinetransform2deffect_setinterpolationmode"]
old-location: directcomp\idcompositionaffinetransform2deffect_setinterpolationmode.htm
tech.root: directcomp
ms.assetid: 29994FF1-F720-4D2A-9B66-1D5E9F1EDFF5
ms.date: 12/05/2018
ms.keywords: IDCompositionAffineTransform2DEffect interface [DirectComposition],SetInterpolationMode method, IDCompositionAffineTransform2DEffect.SetInterpolationMode, IDCompositionAffineTransform2DEffect::SetInterpolationMode, SetInterpolationMode, SetInterpolationMode method [DirectComposition], SetInterpolationMode method [DirectComposition],IDCompositionAffineTransform2DEffect interface, dcomp/IDCompositionAffineTransform2DEffect::SetInterpolationMode, directcomp.idcompositionaffinetransform2deffect_setinterpolationmode
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
 - IDCompositionAffineTransform2DEffect::SetInterpolationMode
 - dcomp/IDCompositionAffineTransform2DEffect::SetInterpolationMode
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
 - IDCompositionAffineTransform2DEffect.SetInterpolationMode
---

# IDCompositionAffineTransform2DEffect::SetInterpolationMode


## -description

Sets the interpolation mode of the effect.

## -parameters

### -param interpolationMode [in]

Type: <b><a href="/windows/desktop/Direct2D/2d-affine-transform">D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE</a></b>

Specifies the interpolation mode of the effect.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionaffinetransform2deffect">IDCompositionAffineTransform2DEffect</a>