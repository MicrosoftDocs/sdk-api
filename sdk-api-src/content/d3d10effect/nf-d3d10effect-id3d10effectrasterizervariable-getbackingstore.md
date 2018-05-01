---
UID: NF:d3d10effect.ID3D10EffectRasterizerVariable.GetBackingStore
title: ID3D10EffectRasterizerVariable::GetBackingStore method
author: windows-driver-content
description: Get a pointer to a variable that contains rasteriser state.
old-location: direct3d10\id3d10effectrasterizervariable_getbackingstore.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrasterizervariable_getbackingstore.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10], ID3D10EffectRasterizerVariable interface, GetBackingStore,ID3D10EffectRasterizerVariable.GetBackingStore, ID3D10EffectRasterizerVariable, ID3D10EffectRasterizerVariable interface [Direct3D 10], GetBackingStore method, ID3D10EffectRasterizerVariable::GetBackingStore, cf2a79ce-7906-f134-2fb4-112e8a4d0de6, d3d10effect/ID3D10EffectRasterizerVariable::GetBackingStore, direct3d10.id3d10effectrasterizervariable_getbackingstore
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectRasterizerVariable.GetBackingStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectRasterizerVariable::GetBackingStore method


## -description


Get a pointer to a variable that contains rasteriser state.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of rasteriser-state descriptions. If there is only one rasteriser variable in the effect, use 0.


### -param pRasterizerDesc [in]

Type: <b><a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">D3D10_RASTERIZER_DESC</a>*</b>

A pointer to a rasteriser-state description (see <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">D3D10_RASTERIZER_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. Backing store data can used to recreate the variable when necessary.




## -see-also




<a href="https://msdn.microsoft.com/f1739480-cade-42fe-aa34-4169b20b3f52">ID3D10EffectRasterizerVariable Interface</a>
 

 

