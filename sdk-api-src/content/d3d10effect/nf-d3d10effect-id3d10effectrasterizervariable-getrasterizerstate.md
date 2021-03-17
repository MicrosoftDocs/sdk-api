---
UID: NF:d3d10effect.ID3D10EffectRasterizerVariable.GetRasterizerState
title: ID3D10EffectRasterizerVariable::GetRasterizerState (d3d10effect.h)
description: Get a pointer to a rasterizer interface.
helpviewer_keywords: ["34eeb6ad-48c0-8ea5-4ad6-2fc879f8d7a1","GetRasterizerState","GetRasterizerState method [Direct3D 10]","GetRasterizerState method [Direct3D 10]","ID3D10EffectRasterizerVariable interface","ID3D10EffectRasterizerVariable interface [Direct3D 10]","GetRasterizerState method","ID3D10EffectRasterizerVariable.GetRasterizerState","ID3D10EffectRasterizerVariable::GetRasterizerState","d3d10effect/ID3D10EffectRasterizerVariable::GetRasterizerState","direct3d10.id3d10effectrasterizervariable_getrasterizerstate"]
old-location: direct3d10\id3d10effectrasterizervariable_getrasterizerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrasterizervariable_getrasterizerstate.htm
ms.date: 12/05/2018
ms.keywords: 34eeb6ad-48c0-8ea5-4ad6-2fc879f8d7a1, GetRasterizerState, GetRasterizerState method [Direct3D 10], GetRasterizerState method [Direct3D 10],ID3D10EffectRasterizerVariable interface, ID3D10EffectRasterizerVariable interface [Direct3D 10],GetRasterizerState method, ID3D10EffectRasterizerVariable.GetRasterizerState, ID3D10EffectRasterizerVariable::GetRasterizerState, d3d10effect/ID3D10EffectRasterizerVariable::GetRasterizerState, direct3d10.id3d10effectrasterizervariable_getrasterizerstate
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
 - ID3D10EffectRasterizerVariable::GetRasterizerState
 - d3d10effect/ID3D10EffectRasterizerVariable::GetRasterizerState
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
 - ID3D10EffectRasterizerVariable.GetRasterizerState
---

# ID3D10EffectRasterizerVariable::GetRasterizerState


## -description

Get a pointer to a rasterizer interface.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of rasterizer interfaces. If there is only one rasterizer interface, use 0.

### -param ppRasterizerState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState</a>**</b>

The address of a pointer to a rasterizer interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrasterizervariable">ID3D10EffectRasterizerVariable Interface</a>