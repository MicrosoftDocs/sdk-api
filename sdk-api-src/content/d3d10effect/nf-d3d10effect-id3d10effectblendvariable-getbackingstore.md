---
UID: NF:d3d10effect.ID3D10EffectBlendVariable.GetBackingStore
title: ID3D10EffectBlendVariable::GetBackingStore (d3d10effect.h)
author: windows-sdk-content
description: Get a pointer to a blend-state variable.
old-location: direct3d10\id3d10effectblendvariable_getbackingstore.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable_getbackingstore.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectBlendVariable interface, ID3D10EffectBlendVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectBlendVariable.GetBackingStore, ID3D10EffectBlendVariable::GetBackingStore, a3cd275e-7fbc-0df7-7bd7-389e7e3c4888, d3d10effect/ID3D10EffectBlendVariable::GetBackingStore, direct3d10.id3d10effectblendvariable_getbackingstore
ms.topic: method
f1_keywords: 
 - "d3d10effect/ID3D10EffectBlendVariable.GetBackingStore"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectBlendVariable::GetBackingStore


## -description


Get a pointer to a blend-state variable.


## -parameters




### -param Index [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of blend-state descriptions. If there is only one blend-state variable in the effect, use 0.


### -param pBlendDesc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">D3D10_BLEND_DESC</a>*</b>

A pointer to a blend-state description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">D3D10_BLEND_DESC</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. Backing store data can used to recreate the variable when necessary.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectblendvariable">ID3D10EffectBlendVariable Interface</a>
 

 

