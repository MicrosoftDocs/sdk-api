---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetMatrixElement(int,int,float)
title: IDCompositionColorMatrixEffect::SetMatrixElement(int,int,float) (dcomp.h)
description: Sets an element of the color matrix. (overload 1/2)
helpviewer_keywords: ["IDCompositionColorMatrixEffect interface [DirectComposition]","SetMatrixElement method","IDCompositionColorMatrixEffect.SetMatrixElement","IDCompositionColorMatrixEffect.SetMatrixElement(int","int","float)","IDCompositionColorMatrixEffect::SetMatrixElement","IDCompositionColorMatrixEffect::SetMatrixElement(int","int","float)","SetMatrixElement","SetMatrixElement method [DirectComposition]","SetMatrixElement method [DirectComposition]","IDCompositionColorMatrixEffect interface","dcomp/IDCompositionColorMatrixEffect::SetMatrixElement","directcomp.idcompositioncolormatrixeffect_setmatrixelement"]
old-location: directcomp\idcompositioncolormatrixeffect_setmatrixelement.htm
tech.root: directcomp
ms.assetid: 4F78FA9F-8115-4D60-B119-F60968AAB1D4
ms.date: 12/05/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetMatrixElement method, IDCompositionColorMatrixEffect.SetMatrixElement, IDCompositionColorMatrixEffect.SetMatrixElement(int,int,float), IDCompositionColorMatrixEffect::SetMatrixElement, IDCompositionColorMatrixEffect::SetMatrixElement(int,int,float), SetMatrixElement, SetMatrixElement method [DirectComposition], SetMatrixElement method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetMatrixElement, directcomp.idcompositioncolormatrixeffect_setmatrixelement
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
 - IDCompositionColorMatrixEffect::SetMatrixElement
 - dcomp/IDCompositionColorMatrixEffect::SetMatrixElement
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
 - IDCompositionColorMatrixEffect.SetMatrixElement
---

# IDCompositionColorMatrixEffect::SetMatrixElement(int,int,float)


## -description

Sets an element of the color matrix.

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

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>
