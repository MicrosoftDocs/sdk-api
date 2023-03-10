---
UID: NF:d3d10effect.ID3D10EffectVariable.AsDepthStencilView
title: ID3D10EffectVariable::AsDepthStencilView (d3d10effect.h)
description: Get a depth-stencil-view variable.
helpviewer_keywords: ["AsDepthStencilView","AsDepthStencilView method [Direct3D 10]","AsDepthStencilView method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsDepthStencilView method","ID3D10EffectVariable.AsDepthStencilView","ID3D10EffectVariable::AsDepthStencilView","cdd98874-51c7-7e0f-20f6-4efe28164ae0","d3d10effect/ID3D10EffectVariable::AsDepthStencilView","direct3d10.id3d10effectvariable_asdepthstencilview"]
old-location: direct3d10\id3d10effectvariable_asdepthstencilview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asdepthstencilview.htm
ms.date: 12/05/2018
ms.keywords: AsDepthStencilView, AsDepthStencilView method [Direct3D 10], AsDepthStencilView method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsDepthStencilView method, ID3D10EffectVariable.AsDepthStencilView, ID3D10EffectVariable::AsDepthStencilView, cdd98874-51c7-7e0f-20f6-4efe28164ae0, d3d10effect/ID3D10EffectVariable::AsDepthStencilView, direct3d10.id3d10effectvariable_asdepthstencilview
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
 - ID3D10EffectVariable::AsDepthStencilView
 - d3d10effect/ID3D10EffectVariable::AsDepthStencilView
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
 - ID3D10EffectVariable.AsDepthStencilView
---

# ID3D10EffectVariable::AsDepthStencilView


## -description

Get a depth-stencil-view variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable">ID3D10EffectDepthStencilViewVariable</a>*</b>

A pointer to a depth-stencil-view variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable">ID3D10EffectDepthStencilViewVariable Interface</a>.

## -remarks

This method returns a version of the effect variable that has been specialized to a depth-stencil-view variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil-view data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
