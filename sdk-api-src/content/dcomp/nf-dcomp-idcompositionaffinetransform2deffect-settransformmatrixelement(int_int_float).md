---
UID: NF:dcomp.IDCompositionAffineTransform2DEffect.SetTransformMatrixElement(int,int,float)
title: IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int,int,float) (dcomp.h)
description: Sets an element of the transform matrix of the effect. (overload 1/2)
helpviewer_keywords: ["IDCompositionAffineTransform2DEffect interface [DirectComposition]","SetTransformMatrixElement method","IDCompositionAffineTransform2DEffect.SetTransformMatrixElement","IDCompositionAffineTransform2DEffect.SetTransformMatrixElement(int","int","float)","IDCompositionAffineTransform2DEffect::SetTransformMatrixElement","IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int","int","float)","SetTransformMatrixElement","SetTransformMatrixElement method [DirectComposition]","SetTransformMatrixElement method [DirectComposition]","IDCompositionAffineTransform2DEffect interface","dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrixElement","directcomp.idcompositionaffinetransform2deffect_settransformmatrixelement"]
old-location: directcomp\idcompositionaffinetransform2deffect_settransformmatrixelement.htm
tech.root: directcomp
ms.assetid: C673951B-2347-4A71-9413-68670B6E11CB
ms.date: 12/05/2018
ms.keywords: IDCompositionAffineTransform2DEffect interface [DirectComposition],SetTransformMatrixElement method, IDCompositionAffineTransform2DEffect.SetTransformMatrixElement, IDCompositionAffineTransform2DEffect.SetTransformMatrixElement(int,int,float), IDCompositionAffineTransform2DEffect::SetTransformMatrixElement, IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int,int,float), SetTransformMatrixElement, SetTransformMatrixElement method [DirectComposition], SetTransformMatrixElement method [DirectComposition],IDCompositionAffineTransform2DEffect interface, dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrixElement, directcomp.idcompositionaffinetransform2deffect_settransformmatrixelement
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
 - IDCompositionAffineTransform2DEffect::SetTransformMatrixElement
 - dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrixElement
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
 - IDCompositionAffineTransform2DEffect.SetTransformMatrixElement
---

# IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int,int,float)


## -description

Sets an element of the transform matrix of the effect.

## -parameters

### -param row [in]

Type: <b>int</b>

The row of the element.

### -param column [in]

Type: <b>int</b>

The column of the element.

### -param value [in]

Type: <b>float</b>

The new value of the element.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionaffinetransform2deffect">IDCompositionAffineTransform2DEffect</a>
