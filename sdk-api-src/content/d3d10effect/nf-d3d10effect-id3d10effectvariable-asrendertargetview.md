---
UID: NF:d3d10effect.ID3D10EffectVariable.AsRenderTargetView
title: ID3D10EffectVariable::AsRenderTargetView (d3d10effect.h)
description: Get a render-target-view variable.
helpviewer_keywords: ["4e1e798b-0790-d8d7-5dc5-8b7d7e7de483","AsRenderTargetView","AsRenderTargetView method [Direct3D 10]","AsRenderTargetView method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsRenderTargetView method","ID3D10EffectVariable.AsRenderTargetView","ID3D10EffectVariable::AsRenderTargetView","d3d10effect/ID3D10EffectVariable::AsRenderTargetView","direct3d10.id3d10effectvariable_asrendertargetview"]
old-location: direct3d10\id3d10effectvariable_asrendertargetview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asrendertargetview.htm
ms.date: 12/05/2018
ms.keywords: 4e1e798b-0790-d8d7-5dc5-8b7d7e7de483, AsRenderTargetView, AsRenderTargetView method [Direct3D 10], AsRenderTargetView method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsRenderTargetView method, ID3D10EffectVariable.AsRenderTargetView, ID3D10EffectVariable::AsRenderTargetView, d3d10effect/ID3D10EffectVariable::AsRenderTargetView, direct3d10.id3d10effectvariable_asrendertargetview
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
 - ID3D10EffectVariable::AsRenderTargetView
 - d3d10effect/ID3D10EffectVariable::AsRenderTargetView
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
 - ID3D10EffectVariable.AsRenderTargetView
---

# ID3D10EffectVariable::AsRenderTargetView


## -description

Get a render-target-view variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrendertargetviewvariable">ID3D10EffectRenderTargetViewVariable</a>*</b>

A pointer to a render-target-view variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrendertargetviewvariable">ID3D10EffectRenderTargetViewVariable Interface</a>.

## -remarks

This method returns a version of the effect variable that has been specialized to a render-target-view variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain render-target-view data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
