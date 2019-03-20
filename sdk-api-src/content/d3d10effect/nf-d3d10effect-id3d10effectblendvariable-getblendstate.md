---
UID: NF:d3d10effect.ID3D10EffectBlendVariable.GetBlendState
title: ID3D10EffectBlendVariable::GetBlendState (d3d10effect.h)
author: windows-sdk-content
description: Get a pointer to a blend-state interface.
old-location: direct3d10\id3d10effectblendvariable_getblendstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable_getblendstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 23f9d59f-d37d-7bdf-874c-f23d35773bb5, GetBlendState, GetBlendState method [Direct3D 10], GetBlendState method [Direct3D 10],ID3D10EffectBlendVariable interface, ID3D10EffectBlendVariable interface [Direct3D 10],GetBlendState method, ID3D10EffectBlendVariable.GetBlendState, ID3D10EffectBlendVariable::GetBlendState, d3d10effect/ID3D10EffectBlendVariable::GetBlendState, direct3d10.id3d10effectblendvariable_getblendstate
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
 - ID3D10EffectBlendVariable.GetBlendState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectBlendVariable::GetBlendState


## -description


Get a pointer to a blend-state interface.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of blend-state interfaces. If there is only one blend-state interface, use 0.


### -param ppBlendState [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173505(v=VS.85).aspx">ID3D10BlendState</a>**</b>

The address of a pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb173505(v=VS.85).aspx">ID3D10BlendState Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173631(v=VS.85).aspx">ID3D10EffectBlendVariable Interface</a>
 

 

