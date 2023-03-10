---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetClampOutput
title: IDCompositionColorMatrixEffect::SetClampOutput (dcomp.h)
description: Specifies whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.
helpviewer_keywords: ["IDCompositionColorMatrixEffect interface [DirectComposition]","SetClampOutput method","IDCompositionColorMatrixEffect.SetClampOutput","IDCompositionColorMatrixEffect::SetClampOutput","SetClampOutput","SetClampOutput method [DirectComposition]","SetClampOutput method [DirectComposition]","IDCompositionColorMatrixEffect interface","dcomp/IDCompositionColorMatrixEffect::SetClampOutput","directcomp.idcompositioncolormatrixeffect_setclampoutput"]
old-location: directcomp\idcompositioncolormatrixeffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: 2C4EF887-18CF-49A2-96F5-02B81939BBA9
ms.date: 12/05/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetClampOutput method, IDCompositionColorMatrixEffect.SetClampOutput, IDCompositionColorMatrixEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetClampOutput, directcomp.idcompositioncolormatrixeffect_setclampoutput
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
 - IDCompositionColorMatrixEffect::SetClampOutput
 - dcomp/IDCompositionColorMatrixEffect::SetClampOutput
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
 - IDCompositionColorMatrixEffect.SetClampOutput
---

# IDCompositionColorMatrixEffect::SetClampOutput


## -description

Specifies whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.

## -parameters

### -param clamp [in]

Type: <b>BOOL</b>

A boolean value indicating whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>