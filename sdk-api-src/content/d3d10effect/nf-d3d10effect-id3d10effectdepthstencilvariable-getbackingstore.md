---
UID: NF:d3d10effect.ID3D10EffectDepthStencilVariable.GetBackingStore
title: ID3D10EffectDepthStencilVariable::GetBackingStore
author: windows-sdk-content
description: Get a pointer to a variable that contains depth-stencil state.
old-location: direct3d10\id3d10effectdepthstencilvariable_getbackingstore.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilvariable_getbackingstore.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetBackingStore, GetBackingStore method [Direct3D 10], GetBackingStore method [Direct3D 10],ID3D10EffectDepthStencilVariable interface, ID3D10EffectDepthStencilVariable interface [Direct3D 10],GetBackingStore method, ID3D10EffectDepthStencilVariable.GetBackingStore, ID3D10EffectDepthStencilVariable::GetBackingStore, d3d10effect/ID3D10EffectDepthStencilVariable::GetBackingStore, direct3d10.id3d10effectdepthstencilvariable_getbackingstore, f9003aa5-ba35-95d6-f8c4-b56aa73c1f4e
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectDepthStencilVariable.GetBackingStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectDepthStencilVariable::GetBackingStore


## -description


Get a pointer to a variable that contains depth-stencil state.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of depth-stencil-state descriptions. If there is only one depth-stencil variable in the effect, use 0.


### -param pDepthStencilDesc [in]

Type: <b><a href="https://msdn.microsoft.com/5337bb50-95ce-47cd-bda5-2828bf3f85d0">D3D10_DEPTH_STENCIL_DESC</a>*</b>

A pointer to a depth-stencil-state description (see <a href="https://msdn.microsoft.com/5337bb50-95ce-47cd-bda5-2828bf3f85d0">D3D10_DEPTH_STENCIL_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. Backing store data can used to recreate the variable when necessary.




## -see-also




<a href="https://msdn.microsoft.com/b8d8fa74-c4fb-4143-a725-741b7d60e0ba">ID3D10EffectDepthStencilVariable Interface</a>
 

 

