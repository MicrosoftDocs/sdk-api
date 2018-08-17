---
UID: NF:d3d10effect.ID3D10EffectDepthStencilVariable.GetDepthStencilState
title: ID3D10EffectDepthStencilVariable::GetDepthStencilState
author: windows-sdk-content
description: Get a pointer to a depth-stencil interface.
old-location: direct3d10\id3d10effectdepthstencilvariable_getdepthstencilstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilvariable_getdepthstencilstate.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 6adcccd9-da86-da4f-0638-3ffb79b7a9de, GetDepthStencilState, GetDepthStencilState method [Direct3D 10], GetDepthStencilState method [Direct3D 10],ID3D10EffectDepthStencilVariable interface, ID3D10EffectDepthStencilVariable interface [Direct3D 10],GetDepthStencilState method, ID3D10EffectDepthStencilVariable.GetDepthStencilState, ID3D10EffectDepthStencilVariable::GetDepthStencilState, d3d10effect/ID3D10EffectDepthStencilVariable::GetDepthStencilState, direct3d10.id3d10effectdepthstencilvariable_getdepthstencilstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectDepthStencilVariable.GetDepthStencilState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectDepthStencilVariable::GetDepthStencilState


## -description


Get a pointer to a depth-stencil interface.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of depth-stencil interfaces. If there is only one depth-stencil interface, use 0.


### -param ppDepthStencilState [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173524(v=VS.85).aspx">ID3D10DepthStencilState</a>**</b>

The address of a pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb173524(v=VS.85).aspx">ID3D10DepthStencilState Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173639(v=VS.85).aspx">ID3D10EffectDepthStencilVariable Interface</a>
 

 

