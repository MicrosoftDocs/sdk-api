---
UID: NF:d3d10effect.ID3D10EffectSamplerVariable.GetSampler
title: ID3D10EffectSamplerVariable::GetSampler
author: windows-sdk-content
description: Get a pointer to a sampler interface.
old-location: direct3d10\id3d10effectsamplervariable_getsampler.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable_getsampler.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetSampler, GetSampler method [Direct3D 10], GetSampler method [Direct3D 10],ID3D10EffectSamplerVariable interface, ID3D10EffectSamplerVariable interface [Direct3D 10],GetSampler method, ID3D10EffectSamplerVariable.GetSampler, ID3D10EffectSamplerVariable::GetSampler, cd07e1d0-28d4-ba10-87d9-3768dd4f0157, d3d10effect/ID3D10EffectSamplerVariable::GetSampler, direct3d10.id3d10effectsamplervariable_getsampler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectSamplerVariable.GetSampler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectSamplerVariable::GetSampler


## -description


Get a pointer to a sampler interface.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of sampler interfaces. If there is only one sampler interface, use 0.


### -param ppSampler [out]

Type: <b><a href="https://msdn.microsoft.com/5815f809-aec0-49b1-bcef-d04146551af9">ID3D10SamplerState</a>**</b>

The address of a pointer to a sampler interface (see <a href="https://msdn.microsoft.com/5815f809-aec0-49b1-bcef-d04146551af9">ID3D10SamplerState Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/1eb8a3be-bf0c-479c-8a59-07a08fb2dc26">ID3D10EffectSamplerVariable Interface</a>
 

 

