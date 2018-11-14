---
UID: NF:d3d10effect.ID3D10EffectSamplerVariable.GetBackingStore
title: ID3D10EffectSamplerVariable::GetBackingStore
author: windows-sdk-content
description: Get a pointer to a variable that contains sampler state.
old-location: direct3d10\id3d10effectsamplervariable_getbackingstore.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable_getbackingstore.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 4dc77fe0-2533-5324-1a51-b4e1cde4e16d, GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectSamplerVariable interface, ID3D10EffectSamplerVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectSamplerVariable.GetBackingStore, ID3D10EffectSamplerVariable::GetBackingStore, d3d10effect/ID3D10EffectSamplerVariable::GetBackingStore, direct3d10.id3d10effectsamplervariable_getbackingstore
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10effect.h
: 
- ID3D10EffectSamplerVariable.GetBackingStore
: 
---

# ID3D10EffectSamplerVariable::GetBackingStore


## -description


Get a pointer to a variable that contains sampler state.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of sampler descriptions. If there is only one sampler variable in the effect, use 0.


### -param pSamplerDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172415(v=VS.85).aspx">D3D10_SAMPLER_DESC</a>*</b>

A pointer to a sampler description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172415(v=VS.85).aspx">D3D10_SAMPLER_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173677(v=VS.85).aspx">ID3D10EffectSamplerVariable Interface</a>
 

 

