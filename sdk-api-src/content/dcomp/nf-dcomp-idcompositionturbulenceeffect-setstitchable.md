---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetStitchable
title: IDCompositionTurbulenceEffect::SetStitchable (dcomp.h)
description: Specifies whether stitching is on or off.
helpviewer_keywords: ["IDCompositionTurbulenceEffect interface [DirectComposition]","SetStitchable method","IDCompositionTurbulenceEffect.SetStitchable","IDCompositionTurbulenceEffect::SetStitchable","SetStitchable","SetStitchable method [DirectComposition]","SetStitchable method [DirectComposition]","IDCompositionTurbulenceEffect interface","dcomp/IDCompositionTurbulenceEffect::SetStitchable","directcomp.idcompositionturbulenceeffect_setstitchable"]
old-location: directcomp\idcompositionturbulenceeffect_setstitchable.htm
tech.root: directcomp
ms.assetid: A73474FD-FECE-4654-8B6C-F44C2DDD7D9C
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetStitchable method, IDCompositionTurbulenceEffect.SetStitchable, IDCompositionTurbulenceEffect::SetStitchable, SetStitchable, SetStitchable method [DirectComposition], SetStitchable method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetStitchable, directcomp.idcompositionturbulenceeffect_setstitchable
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
 - IDCompositionTurbulenceEffect::SetStitchable
 - dcomp/IDCompositionTurbulenceEffect::SetStitchable
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
 - IDCompositionTurbulenceEffect.SetStitchable
---

# IDCompositionTurbulenceEffect::SetStitchable


## -description

Specifies whether stitching is on or off.

## -parameters

### -param stitchable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether stitching is on or off. The base frequency is adjusted so that the output bitmap can be stitched.
            This is useful if you want to tile multiple copies of the turbulence effect output.
            If this value is TRUE, the output bitmap can be tiled (using the tile effect) without the appearance of seams and the base frequency is adjusted so that output bitmap can be stitched.
            If this value is FALSE, the base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>