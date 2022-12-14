---
UID: NF:d3d10effect.ID3D10EffectVariable.AsBlend
title: ID3D10EffectVariable::AsBlend (d3d10effect.h)
description: Get a effect-blend variable.
helpviewer_keywords: ["AsBlend","AsBlend method [Direct3D 10]","AsBlend method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsBlend method","ID3D10EffectVariable.AsBlend","ID3D10EffectVariable::AsBlend","bc3da4a0-2ef6-7ffd-8a6d-1bf74e1ef7da","d3d10effect/ID3D10EffectVariable::AsBlend","direct3d10.id3d10effectvariable_asblend"]
old-location: direct3d10\id3d10effectvariable_asblend.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asblend.htm
ms.date: 12/05/2018
ms.keywords: AsBlend, AsBlend method [Direct3D 10], AsBlend method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsBlend method, ID3D10EffectVariable.AsBlend, ID3D10EffectVariable::AsBlend, bc3da4a0-2ef6-7ffd-8a6d-1bf74e1ef7da, d3d10effect/ID3D10EffectVariable::AsBlend, direct3d10.id3d10effectvariable_asblend
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
 - ID3D10EffectVariable::AsBlend
 - d3d10effect/ID3D10EffectVariable::AsBlend
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
 - ID3D10EffectVariable.AsBlend
---

# ID3D10EffectVariable::AsBlend


## -description

Get a effect-blend variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectblendvariable">ID3D10EffectBlendVariable</a>*</b>

A pointer to an effect blend variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectblendvariable">ID3D10EffectBlendVariable</a>.

## -remarks

AsBlend returns a version of the effect variable that has been specialized to an effect-blend variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain effect-blend data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
