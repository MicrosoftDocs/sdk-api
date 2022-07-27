---
UID: NF:d3d10effect.ID3D10EffectVariable.AsConstantBuffer
title: ID3D10EffectVariable::AsConstantBuffer (d3d10effect.h)
description: Get a constant buffer. (ID3D10EffectVariable.AsConstantBuffer)
helpviewer_keywords: ["477c624a-b604-228f-bba0-0e26ed2d49e1","AsConstantBuffer","AsConstantBuffer method [Direct3D 10]","AsConstantBuffer method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsConstantBuffer method","ID3D10EffectVariable.AsConstantBuffer","ID3D10EffectVariable::AsConstantBuffer","d3d10effect/ID3D10EffectVariable::AsConstantBuffer","direct3d10.id3d10effectvariable_asconstantbuffer"]
old-location: direct3d10\id3d10effectvariable_asconstantbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asconstantbuffer.htm
ms.date: 12/05/2018
ms.keywords: 477c624a-b604-228f-bba0-0e26ed2d49e1, AsConstantBuffer, AsConstantBuffer method [Direct3D 10], AsConstantBuffer method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsConstantBuffer method, ID3D10EffectVariable.AsConstantBuffer, ID3D10EffectVariable::AsConstantBuffer, d3d10effect/ID3D10EffectVariable::AsConstantBuffer, direct3d10.id3d10effectvariable_asconstantbuffer
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
 - ID3D10EffectVariable::AsConstantBuffer
 - d3d10effect/ID3D10EffectVariable::AsConstantBuffer
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
 - ID3D10EffectVariable.AsConstantBuffer
---

# ID3D10EffectVariable::AsConstantBuffer


## -description

Get a constant buffer.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectconstantbuffer">ID3D10EffectConstantBuffer</a>*</b>

A pointer to a constant buffer. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectconstantbuffer">ID3D10EffectConstantBuffer</a>.

## -remarks

AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
