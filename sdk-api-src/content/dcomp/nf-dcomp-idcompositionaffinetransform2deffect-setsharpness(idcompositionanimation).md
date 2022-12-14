---
UID: NF:dcomp.IDCompositionAffineTransform2DEffect.SetSharpness(IDCompositionAnimation)
title: IDCompositionAffineTransform2DEffect::SetSharpness(IDCompositionAnimation) (dcomp.h)
description: Sets the sharpness of the effect. (overload 1/2)
helpviewer_keywords: ["IDCompositionAffineTransform2DEffect interface [DirectComposition]","SetSharpness method","IDCompositionAffineTransform2DEffect.SetSharpness","IDCompositionAffineTransform2DEffect.SetSharpness(IDCompositionAnimation)","IDCompositionAffineTransform2DEffect::SetSharpness","IDCompositionAffineTransform2DEffect::SetSharpness(IDCompositionAnimation)","SetSharpness","SetSharpness method [DirectComposition]","SetSharpness method [DirectComposition]","IDCompositionAffineTransform2DEffect interface","dcomp/IDCompositionAffineTransform2DEffect::SetSharpness","directcomp.idcompositionaffinetransform2deffect_setsharpness_2"]
old-location: directcomp\idcompositionaffinetransform2deffect_setsharpness_2.htm
tech.root: directcomp
ms.assetid: 68369AAC-3EBC-419C-A055-90BF4C662A42
ms.date: 12/05/2018
ms.keywords: IDCompositionAffineTransform2DEffect interface [DirectComposition],SetSharpness method, IDCompositionAffineTransform2DEffect.SetSharpness, IDCompositionAffineTransform2DEffect.SetSharpness(IDCompositionAnimation), IDCompositionAffineTransform2DEffect::SetSharpness, IDCompositionAffineTransform2DEffect::SetSharpness(IDCompositionAnimation), SetSharpness, SetSharpness method [DirectComposition], SetSharpness method [DirectComposition],IDCompositionAffineTransform2DEffect interface, dcomp/IDCompositionAffineTransform2DEffect::SetSharpness, directcomp.idcompositionaffinetransform2deffect_setsharpness_2
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
 - IDCompositionAffineTransform2DEffect::SetSharpness
 - dcomp/IDCompositionAffineTransform2DEffect::SetSharpness
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
 - IDCompositionAffineTransform2DEffect.SetSharpness
---

# IDCompositionAffineTransform2DEffect::SetSharpness(IDCompositionAnimation)


## -description

Sets the sharpness of the effect.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the sharpness value changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionaffinetransform2deffect">IDCompositionAffineTransform2DEffect</a>
