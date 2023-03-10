---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetNoise
title: IDCompositionTurbulenceEffect::SetNoise (dcomp.h)
description: Sets the turbulence noise mode.
helpviewer_keywords: ["IDCompositionTurbulenceEffect interface [DirectComposition]","SetNoise method","IDCompositionTurbulenceEffect.SetNoise","IDCompositionTurbulenceEffect::SetNoise","SetNoise","SetNoise method [DirectComposition]","SetNoise method [DirectComposition]","IDCompositionTurbulenceEffect interface","dcomp/IDCompositionTurbulenceEffect::SetNoise","directcomp.idcompositionturbulenceeffect_setnoise"]
old-location: directcomp\idcompositionturbulenceeffect_setnoise.htm
tech.root: directcomp
ms.assetid: 6EF5C8D0-C614-4520-BAE5-A3C8E609FB64
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetNoise method, IDCompositionTurbulenceEffect.SetNoise, IDCompositionTurbulenceEffect::SetNoise, SetNoise, SetNoise method [DirectComposition], SetNoise method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetNoise, directcomp.idcompositionturbulenceeffect_setnoise
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
 - IDCompositionTurbulenceEffect::SetNoise
 - dcomp/IDCompositionTurbulenceEffect::SetNoise
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
 - IDCompositionTurbulenceEffect.SetNoise
---

# IDCompositionTurbulenceEffect::SetNoise


## -description

Sets the turbulence noise mode.

## -parameters

### -param noise [in]

Type: <b><a href="/windows/desktop/Direct2D/turbulence">D2D1_TURBULENCE_NOISE</a></b>

The turbulence noise mode. Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>