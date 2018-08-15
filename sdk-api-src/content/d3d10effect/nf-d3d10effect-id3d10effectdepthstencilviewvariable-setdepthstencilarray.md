---
UID: NF:d3d10effect.ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray
title: ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray
author: windows-sdk-content
description: Set an array of depth-stencil-view resources.
old-location: direct3d10\id3d10effectdepthstencilviewvariable_setdepthstencilarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilviewvariable_setdepthstencilarray.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 19d677a4-86e6-d451-5d65-7ab228f247d5, ID3D10EffectDepthStencilViewVariable interface [Direct3D 10],SetDepthStencilArray method, ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray, ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray, SetDepthStencilArray, SetDepthStencilArray method [Direct3D 10], SetDepthStencilArray method [Direct3D 10],ID3D10EffectDepthStencilViewVariable interface, d3d10effect/ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray, direct3d10.id3d10effectdepthstencilviewvariable_setdepthstencilarray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: D3d10
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
 - d3d10effect.h
api_name:
 - ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray


## -description


Set an array of depth-stencil-view resources.


## -parameters




### -param ppResources [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView</a>**</b>

A pointer to an array of depth-stencil-view interfaces. See <a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView Interface</a>.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based array index to set the first interface.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements in the array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173642(v=VS.85).aspx">ID3D10EffectDepthStencilViewVariable Interface</a>
 

 

