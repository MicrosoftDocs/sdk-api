---
UID: NF:dcomp.IDCompositionAffineTransform2DEffect.SetTransformMatrix
title: IDCompositionAffineTransform2DEffect::SetTransformMatrix (dcomp.h)
description: Sets the transform matrix of the effect.
helpviewer_keywords: ["IDCompositionAffineTransform2DEffect interface [DirectComposition]","SetTransformMatrix method","IDCompositionAffineTransform2DEffect.SetTransformMatrix","IDCompositionAffineTransform2DEffect::SetTransformMatrix","SetTransformMatrix","SetTransformMatrix method [DirectComposition]","SetTransformMatrix method [DirectComposition]","IDCompositionAffineTransform2DEffect interface","dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrix","directcomp.idcompositionaffinetransform2deffect_settransformmatrix"]
old-location: directcomp\idcompositionaffinetransform2deffect_settransformmatrix.htm
tech.root: directcomp
ms.assetid: C6ED5F96-CA6A-4E96-A368-197242066CC0
ms.date: 12/05/2018
ms.keywords: IDCompositionAffineTransform2DEffect interface [DirectComposition],SetTransformMatrix method, IDCompositionAffineTransform2DEffect.SetTransformMatrix, IDCompositionAffineTransform2DEffect::SetTransformMatrix, SetTransformMatrix, SetTransformMatrix method [DirectComposition], SetTransformMatrix method [DirectComposition],IDCompositionAffineTransform2DEffect interface, dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrix, directcomp.idcompositionaffinetransform2deffect_settransformmatrix
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
 - IDCompositionAffineTransform2DEffect::SetTransformMatrix
 - dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrix
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
 - IDCompositionAffineTransform2DEffect.SetTransformMatrix
---

# IDCompositionAffineTransform2DEffect::SetTransformMatrix


## -description

Sets the transform matrix of the effect.

## -parameters

### -param transformMatrix [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

Specifies the transform matrix for the effect to use.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionaffinetransform2deffect">IDCompositionAffineTransform2DEffect</a>