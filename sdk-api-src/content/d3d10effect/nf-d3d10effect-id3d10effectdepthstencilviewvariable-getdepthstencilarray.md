---
UID: NF:d3d10effect.ID3D10EffectDepthStencilViewVariable.GetDepthStencilArray
title: ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray (d3d10effect.h)
author: windows-sdk-content
description: Get an array of depth-stencil-view resources.
old-location: direct3d10\id3d10effectdepthstencilviewvariable_getdepthstencilarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilviewvariable_getdepthstencilarray.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDepthStencilArray, GetDepthStencilArray method [Direct3D 10], GetDepthStencilArray method [Direct3D 10],ID3D10EffectDepthStencilViewVariable interface, ID3D10EffectDepthStencilViewVariable interface [Direct3D 10],GetDepthStencilArray method, ID3D10EffectDepthStencilViewVariable.GetDepthStencilArray, ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray, c70b6288-bffb-443b-6afe-0fe1168b1cf6, d3d10effect/ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray, direct3d10.id3d10effectdepthstencilviewvariable_getdepthstencilarray
ms.topic: method
f1_keywords: 
 - "d3d10effect/ID3D10EffectDepthStencilViewVariable.GetDepthStencilArray"
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
ms.custom: 19H1
---

# ID3D10EffectDepthStencilViewVariable::GetDepthStencilArray


## -description


Get an array of depth-stencil-view resources.


## -parameters




### -param ppResources [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>**</b>

A pointer to an array of depth-stencil-view interfaces. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView Interface</a>.


### -param Offset [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based array index to get the first interface.


### -param Count [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in the array.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable">ID3D10EffectDepthStencilViewVariable Interface</a>
 

 

