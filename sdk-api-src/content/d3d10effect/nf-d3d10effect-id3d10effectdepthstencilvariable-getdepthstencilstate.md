---
UID: NF:d3d10effect.ID3D10EffectDepthStencilVariable.GetDepthStencilState
title: ID3D10EffectDepthStencilVariable::GetDepthStencilState method
author: windows-driver-content
description: Get a pointer to a depth-stencil interface.
old-location: direct3d10\id3d10effectdepthstencilvariable_getdepthstencilstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilvariable_getdepthstencilstate.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 6adcccd9-da86-da4f-0638-3ffb79b7a9de, GetDepthStencilState method [Direct3D 10], GetDepthStencilState method [Direct3D 10], ID3D10EffectDepthStencilVariable interface, GetDepthStencilState,ID3D10EffectDepthStencilVariable.GetDepthStencilState, ID3D10EffectDepthStencilVariable, ID3D10EffectDepthStencilVariable interface [Direct3D 10], GetDepthStencilState method, ID3D10EffectDepthStencilVariable::GetDepthStencilState, d3d10effect/ID3D10EffectDepthStencilVariable::GetDepthStencilState, direct3d10.id3d10effectdepthstencilvariable_getdepthstencilstate
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
-	ID3D10EffectDepthStencilVariable.GetDepthStencilState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectDepthStencilVariable::GetDepthStencilState method


## -description


Get a pointer to a depth-stencil interface.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of depth-stencil interfaces. If there is only one depth-stencil interface, use 0.


### -param ppDepthStencilState [out]

Type: <b><a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState</a>**</b>

The address of a pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b8d8fa74-c4fb-4143-a725-741b7d60e0ba">ID3D10EffectDepthStencilVariable Interface</a>
 

 

