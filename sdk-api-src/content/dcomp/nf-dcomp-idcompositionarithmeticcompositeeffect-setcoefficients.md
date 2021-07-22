---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficients
title: IDCompositionArithmeticCompositeEffect::SetCoefficients (dcomp.h)
description: Sets the coefficients for the equation used to composite the two input images.
helpviewer_keywords: ["IDCompositionArithmeticCompositeEffect interface [DirectComposition]","SetCoefficients method","IDCompositionArithmeticCompositeEffect.SetCoefficients","IDCompositionArithmeticCompositeEffect::SetCoefficients","SetCoefficients","SetCoefficients method [DirectComposition]","SetCoefficients method [DirectComposition]","IDCompositionArithmeticCompositeEffect interface","dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficients","directcomp.idcompositionarithmeticcompositeeffect_setcoefficients"]
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficients.htm
tech.root: directcomp
ms.assetid: 02A98C38-1D6E-43ED-8744-D3029F4BF573
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficients method, IDCompositionArithmeticCompositeEffect.SetCoefficients, IDCompositionArithmeticCompositeEffect::SetCoefficients, SetCoefficients, SetCoefficients method [DirectComposition], SetCoefficients method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficients, directcomp.idcompositionarithmeticcompositeeffect_setcoefficients
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
 - IDCompositionArithmeticCompositeEffect::SetCoefficients
 - dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficients
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficients
---

# IDCompositionArithmeticCompositeEffect::SetCoefficients


## -description

Sets the coefficients for the equation used to composite the two input images.

## -parameters

### -param coefficients [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a></b>

The coefficients for the equation used to composite the two input images.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>