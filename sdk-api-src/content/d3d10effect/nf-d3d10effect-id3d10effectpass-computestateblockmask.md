---
UID: NF:d3d10effect.ID3D10EffectPass.ComputeStateBlockMask
title: ID3D10EffectPass::ComputeStateBlockMask (d3d10effect.h)
description: Generate a mask for allowing/preventing state changes.
helpviewer_keywords: ["50c69f93-7d81-a766-082e-21f700d2f1ec","ComputeStateBlockMask","ComputeStateBlockMask method [Direct3D 10]","ComputeStateBlockMask method [Direct3D 10]","ID3D10EffectPass interface","ID3D10EffectPass interface [Direct3D 10]","ComputeStateBlockMask method","ID3D10EffectPass.ComputeStateBlockMask","ID3D10EffectPass::ComputeStateBlockMask","d3d10effect/ID3D10EffectPass::ComputeStateBlockMask","direct3d10.id3d10effectpass_computestateblockmask"]
old-location: direct3d10\id3d10effectpass_computestateblockmask.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_computestateblockmask.htm
ms.date: 12/05/2018
ms.keywords: 50c69f93-7d81-a766-082e-21f700d2f1ec, ComputeStateBlockMask, ComputeStateBlockMask method [Direct3D 10], ComputeStateBlockMask method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],ComputeStateBlockMask method, ID3D10EffectPass.ComputeStateBlockMask, ID3D10EffectPass::ComputeStateBlockMask, d3d10effect/ID3D10EffectPass::ComputeStateBlockMask, direct3d10.id3d10effectpass_computestateblockmask
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
 - ID3D10EffectPass::ComputeStateBlockMask
 - d3d10effect/ID3D10EffectPass::ComputeStateBlockMask
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
 - ID3D10EffectPass.ComputeStateBlockMask
---

# ID3D10EffectPass::ComputeStateBlockMask


## -description

Generate a mask for allowing/preventing state changes.

## -parameters

### -param pStateBlockMask [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

A pointer to a state-block mask (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass</a>