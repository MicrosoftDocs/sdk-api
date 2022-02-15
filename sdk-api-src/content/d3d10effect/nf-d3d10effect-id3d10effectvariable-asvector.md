---
UID: NF:d3d10effect.ID3D10EffectVariable.AsVector
title: ID3D10EffectVariable::AsVector (d3d10effect.h)
description: Get a vector variable.
helpviewer_keywords: ["AsVector","AsVector method [Direct3D 10]","AsVector method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsVector method","ID3D10EffectVariable.AsVector","ID3D10EffectVariable::AsVector","a5136c3d-204c-bce5-0022-ead9b334e840","d3d10effect/ID3D10EffectVariable::AsVector","direct3d10.id3d10effectvariable_asvector"]
old-location: direct3d10\id3d10effectvariable_asvector.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asvector.htm
ms.date: 12/05/2018
ms.keywords: AsVector, AsVector method [Direct3D 10], AsVector method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsVector method, ID3D10EffectVariable.AsVector, ID3D10EffectVariable::AsVector, a5136c3d-204c-bce5-0022-ead9b334e840, d3d10effect/ID3D10EffectVariable::AsVector, direct3d10.id3d10effectvariable_asvector
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
 - ID3D10EffectVariable::AsVector
 - d3d10effect/ID3D10EffectVariable::AsVector
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
 - ID3D10EffectVariable.AsVector
---

# ID3D10EffectVariable::AsVector


## -description

Get a vector variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvectorvariable">ID3D10EffectVectorVariable</a>*</b>

A pointer to a vector variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvectorvariable">ID3D10EffectVectorVariable</a>.

## -remarks

AsVector returns a version of the effect variable that has been specialized to a vector variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain vector data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
