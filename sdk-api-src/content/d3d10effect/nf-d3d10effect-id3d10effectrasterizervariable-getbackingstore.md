---
UID: NF:d3d10effect.ID3D10EffectRasterizerVariable.GetBackingStore
title: ID3D10EffectRasterizerVariable::GetBackingStore (d3d10effect.h)
author: windows-sdk-content
description: Get a pointer to a variable that contains rasteriser state.
old-location: direct3d10\id3d10effectrasterizervariable_getbackingstore.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrasterizervariable_getbackingstore.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectRasterizerVariable interface, ID3D10EffectRasterizerVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectRasterizerVariable.GetBackingStore, ID3D10EffectRasterizerVariable::GetBackingStore, cf2a79ce-7906-f134-2fb4-112e8a4d0de6, d3d10effect/ID3D10EffectRasterizerVariable::GetBackingStore, direct3d10.id3d10effectrasterizervariable_getbackingstore
ms.topic: method
f1_keywords: 
 - "d3d10effect/ID3D10EffectRasterizerVariable.GetBackingStore"
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
 - ID3D10EffectRasterizerVariable.GetBackingStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectRasterizerVariable::GetBackingStore


## -description


Get a pointer to a variable that contains rasteriser state.


## -parameters




### -param Index [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into an array of rasteriser-state descriptions. If there is only one rasteriser variable in the effect, use 0.


### -param pRasterizerDesc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>*</b>

A pointer to a rasteriser-state description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. Backing store data can used to recreate the variable when necessary.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrasterizervariable">ID3D10EffectRasterizerVariable Interface</a>
 

 

