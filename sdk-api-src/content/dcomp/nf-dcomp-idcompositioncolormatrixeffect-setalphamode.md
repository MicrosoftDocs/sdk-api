---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetAlphaMode
title: IDCompositionColorMatrixEffect::SetAlphaMode (dcomp.h)
description: Sets the alpha mode of the output for the color matrix effect.
helpviewer_keywords: ["IDCompositionColorMatrixEffect interface [DirectComposition]","SetAlphaMode method","IDCompositionColorMatrixEffect.SetAlphaMode","IDCompositionColorMatrixEffect::SetAlphaMode","SetAlphaMode","SetAlphaMode method [DirectComposition]","SetAlphaMode method [DirectComposition]","IDCompositionColorMatrixEffect interface","dcomp/IDCompositionColorMatrixEffect::SetAlphaMode","directcomp.idcompositioncolormatrixeffect_setalphamode"]
old-location: directcomp\idcompositioncolormatrixeffect_setalphamode.htm
tech.root: directcomp
ms.assetid: BB1464B4-BCF3-4A38-88F0-2B2637DCCBC6
ms.date: 12/05/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetAlphaMode method, IDCompositionColorMatrixEffect.SetAlphaMode, IDCompositionColorMatrixEffect::SetAlphaMode, SetAlphaMode, SetAlphaMode method [DirectComposition], SetAlphaMode method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetAlphaMode, directcomp.idcompositioncolormatrixeffect_setalphamode
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
 - IDCompositionColorMatrixEffect::SetAlphaMode
 - dcomp/IDCompositionColorMatrixEffect::SetAlphaMode
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
 - IDCompositionColorMatrixEffect.SetAlphaMode
---

# IDCompositionColorMatrixEffect::SetAlphaMode


## -description

Sets the alpha mode of the output for the color matrix effect.

## -parameters

### -param mode [in]

Type: <b><a href="/windows/desktop/Direct2D/color-matrix">D2D1_COLORMATRIX_ALPHA_MODE</a></b>

The alpha mode of the output for the color matrix effect.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>