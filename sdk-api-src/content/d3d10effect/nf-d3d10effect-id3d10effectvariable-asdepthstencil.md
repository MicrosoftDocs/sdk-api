---
UID: NF:d3d10effect.ID3D10EffectVariable.AsDepthStencil
title: ID3D10EffectVariable::AsDepthStencil (d3d10effect.h)
description: Get a depth-stencil variable.
helpviewer_keywords: ["AsDepthStencil","AsDepthStencil method [Direct3D 10]","AsDepthStencil method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsDepthStencil method","ID3D10EffectVariable.AsDepthStencil","ID3D10EffectVariable::AsDepthStencil","d12d55ad-aa27-e1e7-7fbd-f7bbe4c54754","d3d10effect/ID3D10EffectVariable::AsDepthStencil","direct3d10.id3d10effectvariable_asdepthstencil"]
old-location: direct3d10\id3d10effectvariable_asdepthstencil.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asdepthstencil.htm
ms.date: 12/05/2018
ms.keywords: AsDepthStencil, AsDepthStencil method [Direct3D 10], AsDepthStencil method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsDepthStencil method, ID3D10EffectVariable.AsDepthStencil, ID3D10EffectVariable::AsDepthStencil, d12d55ad-aa27-e1e7-7fbd-f7bbe4c54754, d3d10effect/ID3D10EffectVariable::AsDepthStencil, direct3d10.id3d10effectvariable_asdepthstencil
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
 - ID3D10EffectVariable::AsDepthStencil
 - d3d10effect/ID3D10EffectVariable::AsDepthStencil
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
 - ID3D10EffectVariable.AsDepthStencil
---

# ID3D10EffectVariable::AsDepthStencil


## -description

Get a depth-stencil variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilvariable">ID3D10EffectDepthStencilVariable</a>*</b>

A pointer to a depth-stencil variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilvariable">ID3D10EffectDepthStencilVariable</a>.

## -remarks

AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
