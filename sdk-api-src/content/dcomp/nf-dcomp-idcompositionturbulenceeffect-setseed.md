---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetSeed
title: IDCompositionTurbulenceEffect::SetSeed (dcomp.h)
description: Sets the seed for the pseudo random generator.
helpviewer_keywords: ["IDCompositionTurbulenceEffect interface [DirectComposition]","SetSeed method","IDCompositionTurbulenceEffect.SetSeed","IDCompositionTurbulenceEffect::SetSeed","SetSeed","SetSeed method [DirectComposition]","SetSeed method [DirectComposition]","IDCompositionTurbulenceEffect interface","dcomp/IDCompositionTurbulenceEffect::SetSeed","directcomp.idcompositionturbulenceeffect_setseed"]
old-location: directcomp\idcompositionturbulenceeffect_setseed.htm
tech.root: directcomp
ms.assetid: FF980DF7-9DD2-4B98-AE84-CB4CA3A1226B
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetSeed method, IDCompositionTurbulenceEffect.SetSeed, IDCompositionTurbulenceEffect::SetSeed, SetSeed, SetSeed method [DirectComposition], SetSeed method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetSeed, directcomp.idcompositionturbulenceeffect_setseed
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
 - IDCompositionTurbulenceEffect::SetSeed
 - dcomp/IDCompositionTurbulenceEffect::SetSeed
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
 - IDCompositionTurbulenceEffect.SetSeed
---

# IDCompositionTurbulenceEffect::SetSeed


## -description

Sets the seed for the pseudo random generator.

## -parameters

### -param seed [in]

Type: <b>UINT</b>

The seed for the pseudo random generator. This value is unbounded.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>