---
UID: NN:d3d10effect.ID3D10EffectSamplerVariable
title: ID3D10EffectSamplerVariable (d3d10effect.h)
description: A sampler interface accesses sampler state.
helpviewer_keywords: ["5f4e0586-ee65-dc10-114c-2c07af8387a7","ID3D10EffectSamplerVariable","ID3D10EffectSamplerVariable interface [Direct3D 10]","ID3D10EffectSamplerVariable interface [Direct3D 10]","described","d3d10effect/ID3D10EffectSamplerVariable","direct3d10.id3d10effectsamplervariable"]
old-location: direct3d10\id3d10effectsamplervariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable.htm
ms.date: 12/05/2018
ms.keywords: 5f4e0586-ee65-dc10-114c-2c07af8387a7, ID3D10EffectSamplerVariable, ID3D10EffectSamplerVariable interface [Direct3D 10], ID3D10EffectSamplerVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectSamplerVariable, direct3d10.id3d10effectsamplervariable
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10EffectSamplerVariable
 - d3d10effect/ID3D10EffectSamplerVariable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10EffectSamplerVariable
---

# ID3D10EffectSamplerVariable interface


## -description

A sampler interface accesses sampler state.

## -inheritance

The <b>ID3D10EffectSamplerVariable</b> interface inherits from <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>. <b>ID3D10EffectSamplerVariable</b> also has these types of members:

## -remarks

An <b>ID3D10EffectSamplerVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-set-state">Two Ways to Get the State in an Effect Variable</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>
