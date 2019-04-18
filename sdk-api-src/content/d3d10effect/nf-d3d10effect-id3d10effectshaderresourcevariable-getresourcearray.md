---
UID: NF:d3d10effect.ID3D10EffectShaderResourceVariable.GetResourceArray
title: ID3D10EffectShaderResourceVariable::GetResourceArray (d3d10effect.h)
author: windows-sdk-content
description: Get an array of shader resources.
old-location: direct3d10\id3d10effectshaderresourcevariable_getresourcearray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshaderresourcevariable_getresourcearray.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetResourceArray, GetResourceArray method [Direct3D 10], GetResourceArray method [Direct3D 10],ID3D10EffectShaderResourceVariable interface, ID3D10EffectShaderResourceVariable interface [Direct3D 10],GetResourceArray method, ID3D10EffectShaderResourceVariable.GetResourceArray, ID3D10EffectShaderResourceVariable::GetResourceArray, be202163-a9e9-5354-d781-12b5b98cda4b, d3d10effect/ID3D10EffectShaderResourceVariable::GetResourceArray, direct3d10.id3d10effectshaderresourcevariable_getresourcearray
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
 - ID3D10EffectShaderResourceVariable.GetResourceArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectShaderResourceVariable::GetResourceArray


## -description


Get an array of shader resources.


## -parameters




### -param ppResources [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView</a>**</b>

The address of an array of shader-resource-view interfaces. See <a href="https://msdn.microsoft.com/en-us/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView Interface</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/Bb173693(v=VS.85).aspx">ID3D10EffectShaderResourceVariable Interface</a>
 

 

