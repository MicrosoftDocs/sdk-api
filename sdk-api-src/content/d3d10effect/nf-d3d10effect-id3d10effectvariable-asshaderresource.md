---
UID: NF:d3d10effect.ID3D10EffectVariable.AsShaderResource
title: ID3D10EffectVariable::AsShaderResource (d3d10effect.h)
description: Get a shader-resource variable.
helpviewer_keywords: ["9ecc402e-7c27-c872-6635-599b5c000326","AsShaderResource","AsShaderResource method [Direct3D 10]","AsShaderResource method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsShaderResource method","ID3D10EffectVariable.AsShaderResource","ID3D10EffectVariable::AsShaderResource","d3d10effect/ID3D10EffectVariable::AsShaderResource","direct3d10.id3d10effectvariable_asshaderresource"]
old-location: direct3d10\id3d10effectvariable_asshaderresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asshaderresource.htm
ms.date: 12/05/2018
ms.keywords: 9ecc402e-7c27-c872-6635-599b5c000326, AsShaderResource, AsShaderResource method [Direct3D 10], AsShaderResource method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsShaderResource method, ID3D10EffectVariable.AsShaderResource, ID3D10EffectVariable::AsShaderResource, d3d10effect/ID3D10EffectVariable::AsShaderResource, direct3d10.id3d10effectvariable_asshaderresource
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
 - ID3D10EffectVariable::AsShaderResource
 - d3d10effect/ID3D10EffectVariable::AsShaderResource
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
 - ID3D10EffectVariable.AsShaderResource
---

# ID3D10EffectVariable::AsShaderResource


## -description

Get a shader-resource variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable</a>*</b>

A pointer to a shader-resource variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable</a>.

## -remarks

AsShaderResource returns a version of the effect variable that has been specialized to a shader-resource variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader-resource data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
