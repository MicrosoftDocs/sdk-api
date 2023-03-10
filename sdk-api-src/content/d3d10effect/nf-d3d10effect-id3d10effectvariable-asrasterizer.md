---
UID: NF:d3d10effect.ID3D10EffectVariable.AsRasterizer
title: ID3D10EffectVariable::AsRasterizer (d3d10effect.h)
description: Get a rasterizer variable.
helpviewer_keywords: ["0306e054-b8c5-9b23-2bcb-82e72a683879","AsRasterizer","AsRasterizer method [Direct3D 10]","AsRasterizer method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsRasterizer method","ID3D10EffectVariable.AsRasterizer","ID3D10EffectVariable::AsRasterizer","d3d10effect/ID3D10EffectVariable::AsRasterizer","direct3d10.id3d10effectvariable_asrasterizer"]
old-location: direct3d10\id3d10effectvariable_asrasterizer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asrasterizer.htm
ms.date: 12/05/2018
ms.keywords: 0306e054-b8c5-9b23-2bcb-82e72a683879, AsRasterizer, AsRasterizer method [Direct3D 10], AsRasterizer method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsRasterizer method, ID3D10EffectVariable.AsRasterizer, ID3D10EffectVariable::AsRasterizer, d3d10effect/ID3D10EffectVariable::AsRasterizer, direct3d10.id3d10effectvariable_asrasterizer
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
 - ID3D10EffectVariable::AsRasterizer
 - d3d10effect/ID3D10EffectVariable::AsRasterizer
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
 - ID3D10EffectVariable.AsRasterizer
---

# ID3D10EffectVariable::AsRasterizer


## -description

Get a rasterizer variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrasterizervariable">ID3D10EffectRasterizerVariable</a>*</b>

A pointer to a rasterizer variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrasterizervariable">ID3D10EffectRasterizerVariable</a>.

## -remarks

AsRasterizer returns a version of the effect variable that has been specialized to a rasterizer variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain rasterizer data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
