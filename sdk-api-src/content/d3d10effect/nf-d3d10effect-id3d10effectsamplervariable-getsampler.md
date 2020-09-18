---
UID: NF:d3d10effect.ID3D10EffectSamplerVariable.GetSampler
title: ID3D10EffectSamplerVariable::GetSampler (d3d10effect.h)
description: Get a pointer to a sampler interface.
helpviewer_keywords: ["GetSampler","GetSampler method [Direct3D 10]","GetSampler method [Direct3D 10]","ID3D10EffectSamplerVariable interface","ID3D10EffectSamplerVariable interface [Direct3D 10]","GetSampler method","ID3D10EffectSamplerVariable.GetSampler","ID3D10EffectSamplerVariable::GetSampler","cd07e1d0-28d4-ba10-87d9-3768dd4f0157","d3d10effect/ID3D10EffectSamplerVariable::GetSampler","direct3d10.id3d10effectsamplervariable_getsampler"]
old-location: direct3d10\id3d10effectsamplervariable_getsampler.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable_getsampler.htm
ms.date: 12/05/2018
ms.keywords: GetSampler, GetSampler method [Direct3D 10], GetSampler method [Direct3D 10],ID3D10EffectSamplerVariable interface, ID3D10EffectSamplerVariable interface [Direct3D 10],GetSampler method, ID3D10EffectSamplerVariable.GetSampler, ID3D10EffectSamplerVariable::GetSampler, cd07e1d0-28d4-ba10-87d9-3768dd4f0157, d3d10effect/ID3D10EffectSamplerVariable::GetSampler, direct3d10.id3d10effectsamplervariable_getsampler
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
 - ID3D10EffectSamplerVariable::GetSampler
 - d3d10effect/ID3D10EffectSamplerVariable::GetSampler
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
 - ID3D10EffectSamplerVariable.GetSampler
---

# ID3D10EffectSamplerVariable::GetSampler


## -description

Get a pointer to a sampler interface.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of sampler interfaces. If there is only one sampler interface, use 0.

### -param ppSampler [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState</a>**</b>

The address of a pointer to a sampler interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectsamplervariable">ID3D10EffectSamplerVariable Interface</a>