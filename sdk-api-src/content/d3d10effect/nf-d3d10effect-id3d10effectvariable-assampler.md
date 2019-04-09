---
UID: NF:d3d10effect.ID3D10EffectVariable.AsSampler
title: ID3D10EffectVariable::AsSampler (d3d10effect.h)
author: windows-sdk-content
description: Get a sampler variable.
old-location: direct3d10\id3d10effectvariable_assampler.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_assampler.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 88e24adb-ffd5-8d00-851b-316db16c8da8, AsSampler, AsSampler method [Direct3D 10], AsSampler method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsSampler method, ID3D10EffectVariable.AsSampler, ID3D10EffectVariable::AsSampler, d3d10effect/ID3D10EffectVariable::AsSampler, direct3d10.id3d10effectvariable_assampler
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
---

# ID3D10EffectVariable::AsSampler


## -description


Get a sampler variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173677(v=VS.85).aspx">ID3D10EffectSamplerVariable</a>*</b>

A pointer to a sampler variable. See <a href="https://msdn.microsoft.com/en-us/library/Bb173677(v=VS.85).aspx">ID3D10EffectSamplerVariable</a>.




## -remarks



AsSampler returns a version of the effect variable that has been specialized to a sampler variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain sampler data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

