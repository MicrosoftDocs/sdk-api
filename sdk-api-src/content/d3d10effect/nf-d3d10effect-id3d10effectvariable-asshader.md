---
UID: NF:d3d10effect.ID3D10EffectVariable.AsShader
title: ID3D10EffectVariable::AsShader (d3d10effect.h)
description: Get a shader variable.
helpviewer_keywords: ["AsShader","AsShader method [Direct3D 10]","AsShader method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsShader method","ID3D10EffectVariable.AsShader","ID3D10EffectVariable::AsShader","cfb94875-697a-f808-87e1-768dc74cc207","d3d10effect/ID3D10EffectVariable::AsShader","direct3d10.id3d10effectvariable_asshader"]
old-location: direct3d10\id3d10effectvariable_asshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asshader.htm
ms.date: 12/05/2018
ms.keywords: AsShader, AsShader method [Direct3D 10], AsShader method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsShader method, ID3D10EffectVariable.AsShader, ID3D10EffectVariable::AsShader, cfb94875-697a-f808-87e1-768dc74cc207, d3d10effect/ID3D10EffectVariable::AsShader, direct3d10.id3d10effectvariable_asshader
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
 - ID3D10EffectVariable::AsShader
 - d3d10effect/ID3D10EffectVariable::AsShader
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
 - ID3D10EffectVariable.AsShader
---

# ID3D10EffectVariable::AsShader


## -description

Get a shader variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>*</b>

A pointer to a shader variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>.

## -remarks

AsShader returns a version of the effect variable that has been specialized to a shader variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
