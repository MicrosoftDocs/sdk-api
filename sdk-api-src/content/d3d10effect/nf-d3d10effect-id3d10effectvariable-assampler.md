---
UID: NF:d3d10effect.ID3D10EffectVariable.AsSampler
title: ID3D10EffectVariable::AsSampler
author: windows-sdk-content
description: Get a sampler variable.
old-location: direct3d10\id3d10effectvariable_assampler.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_assampler.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 88e24adb-ffd5-8d00-851b-316db16c8da8, AsSampler, AsSampler method [Direct3D 10], AsSampler method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsSampler method, ID3D10EffectVariable.AsSampler, ID3D10EffectVariable::AsSampler, d3d10effect/ID3D10EffectVariable::AsSampler, direct3d10.id3d10effectvariable_assampler
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
 - ID3D10EffectVariable.AsSampler
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
- ID3D10EffectVariable.AsSampler
: 
---

# ID3D10EffectVariable::AsSampler


## -description


Get a sampler variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/1eb8a3be-bf0c-479c-8a59-07a08fb2dc26">ID3D10EffectSamplerVariable</a>*</b>

A pointer to a sampler variable. See <a href="https://msdn.microsoft.com/1eb8a3be-bf0c-479c-8a59-07a08fb2dc26">ID3D10EffectSamplerVariable</a>.




## -remarks



AsSampler returns a version of the effect variable that has been specialized to a sampler variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain sampler data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

