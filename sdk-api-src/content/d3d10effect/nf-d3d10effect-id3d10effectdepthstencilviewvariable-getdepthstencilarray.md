---
UID: NF:d3d10effect.ID3D10EffectDepthStencilViewVariable.GetDepthStencilArray
title: ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray
author: windows-sdk-content
description: Get an array of depth-stencil-view resources.
old-location: direct3d10\id3d10effectdepthstencilviewvariable_getdepthstencilarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilviewvariable_getdepthstencilarray.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetDepthStencilArray, GetDepthStencilArray method [Direct3D 10], GetDepthStencilArray method [Direct3D 10],ID3D10EffectDepthStencilViewVariable interface, ID3D10EffectDepthStencilViewVariable interface [Direct3D 10],GetDepthStencilArray method, ID3D10EffectDepthStencilViewVariable.GetDepthStencilArray, ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray, c70b6288-bffb-443b-6afe-0fe1168b1cf6, d3d10effect/ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray, direct3d10.id3d10effectdepthstencilviewvariable_getdepthstencilarray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10effect.h
req.include-header: D3d10
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
 - d3d10effect.h
api_name:
 - ID3D10EffectDepthStencilViewVariable.GetDepthStencilArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray


## -description


Get an array of depth-stencil-view resources.


## -parameters




### -param ppResources [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView</a>**</b>

A pointer to an array of depth-stencil-view interfaces. See <a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView Interface</a>.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based array index to get the first interface.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements in the array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173642(v=VS.85).aspx">ID3D10EffectDepthStencilViewVariable Interface</a>
 

 

