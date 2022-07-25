---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetNumOctaves
title: IDCompositionTurbulenceEffect::SetNumOctaves (dcomp.h)
description: Sets the number of octaves for the noise function.
helpviewer_keywords: ["IDCompositionTurbulenceEffect interface [DirectComposition]","SetNumOctaves method","IDCompositionTurbulenceEffect.SetNumOctaves","IDCompositionTurbulenceEffect::SetNumOctaves","SetNumOctaves","SetNumOctaves method [DirectComposition]","SetNumOctaves method [DirectComposition]","IDCompositionTurbulenceEffect interface","dcomp/IDCompositionTurbulenceEffect::SetNumOctaves","directcomp.idcompositionturbulenceeffect_setnumoctaves"]
old-location: directcomp\idcompositionturbulenceeffect_setnumoctaves.htm
tech.root: directcomp
ms.assetid: 759F03F2-4CA2-454D-8AAE-C18B5E3FD3D0
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetNumOctaves method, IDCompositionTurbulenceEffect.SetNumOctaves, IDCompositionTurbulenceEffect::SetNumOctaves, SetNumOctaves, SetNumOctaves method [DirectComposition], SetNumOctaves method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetNumOctaves, directcomp.idcompositionturbulenceeffect_setnumoctaves
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
 - IDCompositionTurbulenceEffect::SetNumOctaves
 - dcomp/IDCompositionTurbulenceEffect::SetNumOctaves
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
 - IDCompositionTurbulenceEffect.SetNumOctaves
---

# IDCompositionTurbulenceEffect::SetNumOctaves


## -description

Sets the number of octaves for the noise function.

## -parameters

### -param numOctaves [in]

Type: <b>UINT</b>

The number of octaves for the noise function. This value must be greater than 0.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>