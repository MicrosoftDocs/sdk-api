---
UID: NF:d3d10effect.ID3D10EffectBlendVariable.GetBackingStore
title: ID3D10EffectBlendVariable::GetBackingStore
author: windows-sdk-content
description: Get a pointer to a blend-state variable.
old-location: direct3d10\id3d10effectblendvariable_getbackingstore.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable_getbackingstore.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectBlendVariable interface, ID3D10EffectBlendVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectBlendVariable.GetBackingStore, ID3D10EffectBlendVariable::GetBackingStore, a3cd275e-7fbc-0df7-7bd7-389e7e3c4888, d3d10effect/ID3D10EffectBlendVariable::GetBackingStore, direct3d10.id3d10effectblendvariable_getbackingstore
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
 - ID3D10EffectBlendVariable.GetBackingStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectBlendVariable::GetBackingStore


## -description


Get a pointer to a blend-state variable.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of blend-state descriptions. If there is only one blend-state variable in the effect, use 0.


### -param pBlendDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204893(v=VS.85).aspx">D3D10_BLEND_DESC</a>*</b>

A pointer to a blend-state description (see <a href="https://msdn.microsoft.com/en-us/library/Bb204893(v=VS.85).aspx">D3D10_BLEND_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. Backing store data can used to recreate the variable when necessary.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173631(v=VS.85).aspx">ID3D10EffectBlendVariable Interface</a>
 

 

