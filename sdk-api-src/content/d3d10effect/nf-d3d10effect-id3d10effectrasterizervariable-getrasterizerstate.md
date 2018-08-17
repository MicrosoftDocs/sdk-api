---
UID: NF:d3d10effect.ID3D10EffectRasterizerVariable.GetRasterizerState
title: ID3D10EffectRasterizerVariable::GetRasterizerState
author: windows-sdk-content
description: Get a pointer to a rasterizer interface.
old-location: direct3d10\id3d10effectrasterizervariable_getrasterizerstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrasterizervariable_getrasterizerstate.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 34eeb6ad-48c0-8ea5-4ad6-2fc879f8d7a1, GetRasterizerState, GetRasterizerState method [Direct3D 10], GetRasterizerState method [Direct3D 10],ID3D10EffectRasterizerVariable interface, ID3D10EffectRasterizerVariable interface [Direct3D 10],GetRasterizerState method, ID3D10EffectRasterizerVariable.GetRasterizerState, ID3D10EffectRasterizerVariable::GetRasterizerState, d3d10effect/ID3D10EffectRasterizerVariable::GetRasterizerState, direct3d10.id3d10effectrasterizervariable_getrasterizerstate
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
 - ID3D10EffectRasterizerVariable.GetRasterizerState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectRasterizerVariable::GetRasterizerState


## -description


Get a pointer to a rasterizer interface.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of rasterizer interfaces. If there is only one rasterizer interface, use 0.


### -param ppRasterizerState [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173825(v=VS.85).aspx">ID3D10RasterizerState</a>**</b>

The address of a pointer to a rasterizer interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb173825(v=VS.85).aspx">ID3D10RasterizerState Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173669(v=VS.85).aspx">ID3D10EffectRasterizerVariable Interface</a>
 

 

