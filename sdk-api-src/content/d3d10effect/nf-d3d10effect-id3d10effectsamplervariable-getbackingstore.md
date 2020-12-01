---
UID: NF:d3d10effect.ID3D10EffectSamplerVariable.GetBackingStore
title: ID3D10EffectSamplerVariable::GetBackingStore (d3d10effect.h)
description: Get a pointer to a variable that contains sampler state.
helpviewer_keywords: ["4dc77fe0-2533-5324-1a51-b4e1cde4e16d","GetBackingStore","GetBackingStore method [Direct3D 10]","GetBackingStore method [Direct3D 10]","ID3D10EffectSamplerVariable interface","ID3D10EffectSamplerVariable interface [Direct3D 10]","GetBackingStore method","ID3D10EffectSamplerVariable.GetBackingStore","ID3D10EffectSamplerVariable::GetBackingStore","d3d10effect/ID3D10EffectSamplerVariable::GetBackingStore","direct3d10.id3d10effectsamplervariable_getbackingstore"]
old-location: direct3d10\id3d10effectsamplervariable_getbackingstore.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable_getbackingstore.htm
ms.date: 12/05/2018
ms.keywords: 4dc77fe0-2533-5324-1a51-b4e1cde4e16d, GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectSamplerVariable interface, ID3D10EffectSamplerVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectSamplerVariable.GetBackingStore, ID3D10EffectSamplerVariable::GetBackingStore, d3d10effect/ID3D10EffectSamplerVariable::GetBackingStore, direct3d10.id3d10effectsamplervariable_getbackingstore
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
 - ID3D10EffectSamplerVariable::GetBackingStore
 - d3d10effect/ID3D10EffectSamplerVariable::GetBackingStore
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
 - ID3D10EffectSamplerVariable.GetBackingStore
---

# ID3D10EffectSamplerVariable::GetBackingStore


## -description

Get a pointer to a variable that contains sampler state.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of sampler descriptions. If there is only one sampler variable in the effect, use 0.

### -param pSamplerDesc [in]

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc">D3D10_SAMPLER_DESC</a>*</b>

A pointer to a sampler description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc">D3D10_SAMPLER_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectsamplervariable">ID3D10EffectSamplerVariable Interface</a>