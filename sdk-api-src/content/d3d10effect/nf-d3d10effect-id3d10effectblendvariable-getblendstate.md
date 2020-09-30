---
UID: NF:d3d10effect.ID3D10EffectBlendVariable.GetBlendState
title: ID3D10EffectBlendVariable::GetBlendState (d3d10effect.h)
description: Get a pointer to a blend-state interface.
helpviewer_keywords: ["23f9d59f-d37d-7bdf-874c-f23d35773bb5","GetBlendState","GetBlendState method [Direct3D 10]","GetBlendState method [Direct3D 10]","ID3D10EffectBlendVariable interface","ID3D10EffectBlendVariable interface [Direct3D 10]","GetBlendState method","ID3D10EffectBlendVariable.GetBlendState","ID3D10EffectBlendVariable::GetBlendState","d3d10effect/ID3D10EffectBlendVariable::GetBlendState","direct3d10.id3d10effectblendvariable_getblendstate"]
old-location: direct3d10\id3d10effectblendvariable_getblendstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable_getblendstate.htm
ms.date: 12/05/2018
ms.keywords: 23f9d59f-d37d-7bdf-874c-f23d35773bb5, GetBlendState, GetBlendState method [Direct3D 10], GetBlendState method [Direct3D 10],ID3D10EffectBlendVariable interface, ID3D10EffectBlendVariable interface [Direct3D 10],GetBlendState method, ID3D10EffectBlendVariable.GetBlendState, ID3D10EffectBlendVariable::GetBlendState, d3d10effect/ID3D10EffectBlendVariable::GetBlendState, direct3d10.id3d10effectblendvariable_getblendstate
req.header: d3d10effect.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10EffectBlendVariable::GetBlendState
 - d3d10effect/ID3D10EffectBlendVariable::GetBlendState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectBlendVariable.GetBlendState
---

# ID3D10EffectBlendVariable::GetBlendState


## -description

Get a pointer to a blend-state interface.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of blend-state interfaces. If there is only one blend-state interface, use 0.

### -param ppBlendState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState</a>**</b>

The address of a pointer to a blend-state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectblendvariable">ID3D10EffectBlendVariable Interface</a>