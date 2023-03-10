---
UID: NN:d3d10effect.ID3D10EffectDepthStencilVariable
title: ID3D10EffectDepthStencilVariable (d3d10effect.h)
description: A depth-stencil-variable interface accesses depth-stencil state.
helpviewer_keywords: ["896bf0ca-5516-5a5a-b85d-a24c6e618bc1","ID3D10EffectDepthStencilVariable","ID3D10EffectDepthStencilVariable interface [Direct3D 10]","ID3D10EffectDepthStencilVariable interface [Direct3D 10]","described","d3d10effect/ID3D10EffectDepthStencilVariable","direct3d10.id3d10effectdepthstencilvariable"]
old-location: direct3d10\id3d10effectdepthstencilvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilvariable.htm
ms.date: 12/05/2018
ms.keywords: 896bf0ca-5516-5a5a-b85d-a24c6e618bc1, ID3D10EffectDepthStencilVariable, ID3D10EffectDepthStencilVariable interface [Direct3D 10], ID3D10EffectDepthStencilVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectDepthStencilVariable, direct3d10.id3d10effectdepthstencilvariable
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
 - ID3D10EffectDepthStencilVariable
 - d3d10effect/ID3D10EffectDepthStencilVariable
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
 - ID3D10EffectDepthStencilVariable
---

# ID3D10EffectDepthStencilVariable interface


## -description

A depth-stencil-variable interface accesses depth-stencil state.

## -inheritance

The <b>ID3D10EffectDepthStencilVariable</b> interface inherits from <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>. <b>ID3D10EffectDepthStencilVariable</b> also has these types of members:

## -remarks

An <b>ID3D10EffectDepthStencilVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-set-state">Two Ways to Get the State in an Effect Variable</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>
