---
UID: NN:d3d10effect.ID3D10EffectBlendVariable
title: ID3D10EffectBlendVariable (d3d10effect.h)
description: The blend-variable interface accesses blend state.
helpviewer_keywords: ["5dc3aa3a-6996-e7d4-76dc-917fe69d9260","ID3D10EffectBlendVariable","ID3D10EffectBlendVariable interface [Direct3D 10]","ID3D10EffectBlendVariable interface [Direct3D 10]","described","d3d10effect/ID3D10EffectBlendVariable","direct3d10.id3d10effectblendvariable"]
old-location: direct3d10\id3d10effectblendvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable.htm
ms.date: 12/05/2018
ms.keywords: 5dc3aa3a-6996-e7d4-76dc-917fe69d9260, ID3D10EffectBlendVariable, ID3D10EffectBlendVariable interface [Direct3D 10], ID3D10EffectBlendVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectBlendVariable, direct3d10.id3d10effectblendvariable
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
 - ID3D10EffectBlendVariable
 - d3d10effect/ID3D10EffectBlendVariable
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
 - ID3D10EffectBlendVariable
---

# ID3D10EffectBlendVariable interface


## -description

The blend-variable interface accesses blend state.

## -inheritance

The <b>ID3D10EffectBlendVariable</b> interface inherits from <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>. <b>ID3D10EffectBlendVariable</b> also has these types of members:

## -remarks

An <b>ID3D10EffectBlendVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-set-state">Two Ways to Get the State in an Effect Variable</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>
