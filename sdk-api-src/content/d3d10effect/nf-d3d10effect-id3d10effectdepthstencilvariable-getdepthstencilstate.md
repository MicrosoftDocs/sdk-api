---
UID: NF:d3d10effect.ID3D10EffectDepthStencilVariable.GetDepthStencilState
title: ID3D10EffectDepthStencilVariable::GetDepthStencilState (d3d10effect.h)
description: Get a pointer to a depth-stencil interface.
helpviewer_keywords: ["6adcccd9-da86-da4f-0638-3ffb79b7a9de","GetDepthStencilState","GetDepthStencilState method [Direct3D 10]","GetDepthStencilState method [Direct3D 10]","ID3D10EffectDepthStencilVariable interface","ID3D10EffectDepthStencilVariable interface [Direct3D 10]","GetDepthStencilState method","ID3D10EffectDepthStencilVariable.GetDepthStencilState","ID3D10EffectDepthStencilVariable::GetDepthStencilState","d3d10effect/ID3D10EffectDepthStencilVariable::GetDepthStencilState","direct3d10.id3d10effectdepthstencilvariable_getdepthstencilstate"]
old-location: direct3d10\id3d10effectdepthstencilvariable_getdepthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilvariable_getdepthstencilstate.htm
ms.date: 12/05/2018
ms.keywords: 6adcccd9-da86-da4f-0638-3ffb79b7a9de, GetDepthStencilState, GetDepthStencilState method [Direct3D 10], GetDepthStencilState method [Direct3D 10],ID3D10EffectDepthStencilVariable interface, ID3D10EffectDepthStencilVariable interface [Direct3D 10],GetDepthStencilState method, ID3D10EffectDepthStencilVariable.GetDepthStencilState, ID3D10EffectDepthStencilVariable::GetDepthStencilState, d3d10effect/ID3D10EffectDepthStencilVariable::GetDepthStencilState, direct3d10.id3d10effectdepthstencilvariable_getdepthstencilstate
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
 - ID3D10EffectDepthStencilVariable::GetDepthStencilState
 - d3d10effect/ID3D10EffectDepthStencilVariable::GetDepthStencilState
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
 - ID3D10EffectDepthStencilVariable.GetDepthStencilState
---

# ID3D10EffectDepthStencilVariable::GetDepthStencilState


## -description

Get a pointer to a depth-stencil interface.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of depth-stencil interfaces. If there is only one depth-stencil interface, use 0.

### -param ppDepthStencilState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilstate">ID3D10DepthStencilState</a>**</b>

The address of a pointer to a blend-state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilstate">ID3D10DepthStencilState Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilvariable">ID3D10EffectDepthStencilVariable Interface</a>