---
UID: NF:d3d10effect.ID3D10EffectTechnique.ComputeStateBlockMask
title: ID3D10EffectTechnique::ComputeStateBlockMask (d3d10effect.h)
description: Compute a state-block mask to allow/prevent state changes.
helpviewer_keywords: ["ComputeStateBlockMask","ComputeStateBlockMask method [Direct3D 10]","ComputeStateBlockMask method [Direct3D 10]","ID3D10EffectTechnique interface","ID3D10EffectTechnique interface [Direct3D 10]","ComputeStateBlockMask method","ID3D10EffectTechnique.ComputeStateBlockMask","ID3D10EffectTechnique::ComputeStateBlockMask","d3d10effect/ID3D10EffectTechnique::ComputeStateBlockMask","direct3d10.id3d10effecttechnique_computestateblockmask","edde0246-0e4d-7194-97eb-796b3e11860c"]
old-location: direct3d10\id3d10effecttechnique_computestateblockmask.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique_computestateblockmask.htm
ms.date: 12/05/2018
ms.keywords: ComputeStateBlockMask, ComputeStateBlockMask method [Direct3D 10], ComputeStateBlockMask method [Direct3D 10],ID3D10EffectTechnique interface, ID3D10EffectTechnique interface [Direct3D 10],ComputeStateBlockMask method, ID3D10EffectTechnique.ComputeStateBlockMask, ID3D10EffectTechnique::ComputeStateBlockMask, d3d10effect/ID3D10EffectTechnique::ComputeStateBlockMask, direct3d10.id3d10effecttechnique_computestateblockmask, edde0246-0e4d-7194-97eb-796b3e11860c
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
 - ID3D10EffectTechnique::ComputeStateBlockMask
 - d3d10effect/ID3D10EffectTechnique::ComputeStateBlockMask
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
 - ID3D10EffectTechnique.ComputeStateBlockMask
---

# ID3D10EffectTechnique::ComputeStateBlockMask


## -description

Compute a state-block mask to allow/prevent state changes.

## -parameters

### -param pStateBlockMask [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

A pointer to a state-block mask (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effecttechnique">ID3D10EffectTechnique Interface</a>