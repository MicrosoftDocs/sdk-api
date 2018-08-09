---
UID: NF:d3d10effect.ID3D10EffectSamplerVariable.GetBackingStore
title: ID3D10EffectSamplerVariable::GetBackingStore
author: windows-sdk-content
description: Get a pointer to a variable that contains sampler state.
old-location: direct3d10\id3d10effectsamplervariable_getbackingstore.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable_getbackingstore.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 4dc77fe0-2533-5324-1a51-b4e1cde4e16d, GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectSamplerVariable interface, ID3D10EffectSamplerVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectSamplerVariable.GetBackingStore, ID3D10EffectSamplerVariable::GetBackingStore, d3d10effect/ID3D10EffectSamplerVariable::GetBackingStore, direct3d10.id3d10effectsamplervariable_getbackingstore
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
 - ID3D10EffectSamplerVariable.GetBackingStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectSamplerVariable::GetBackingStore


## -description


Get a pointer to a variable that contains sampler state.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of sampler descriptions. If there is only one sampler variable in the effect, use 0.


### -param pSamplerDesc [in]

Type: <b><a href="https://msdn.microsoft.com/b97db311-de57-45f3-a6dd-8af768b2680d">D3D10_SAMPLER_DESC</a>*</b>

A pointer to a sampler description (see <a href="https://msdn.microsoft.com/b97db311-de57-45f3-a6dd-8af768b2680d">D3D10_SAMPLER_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/1eb8a3be-bf0c-479c-8a59-07a08fb2dc26">ID3D10EffectSamplerVariable Interface</a>
 

 

