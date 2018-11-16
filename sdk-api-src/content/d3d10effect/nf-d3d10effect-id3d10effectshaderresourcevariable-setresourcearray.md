---
UID: NF:d3d10effect.ID3D10EffectShaderResourceVariable.SetResourceArray
title: ID3D10EffectShaderResourceVariable::SetResourceArray
author: windows-sdk-content
description: Set an array of shader resources.
old-location: direct3d10\id3d10effectshaderresourcevariable_setresourcearray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshaderresourcevariable_setresourcearray.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D10EffectShaderResourceVariable interface [Direct3D 10],SetResourceArray method, ID3D10EffectShaderResourceVariable.SetResourceArray, ID3D10EffectShaderResourceVariable::SetResourceArray, SetResourceArray, SetResourceArray method [Direct3D 10], SetResourceArray method [Direct3D 10],ID3D10EffectShaderResourceVariable interface, d3d10effect/ID3D10EffectShaderResourceVariable::SetResourceArray, direct3d10.id3d10effectshaderresourcevariable_setresourcearray, ffaa0326-c3e6-873d-a783-a06195e76351
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
 - ID3D10EffectShaderResourceVariable.SetResourceArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10effect.h
: 
- ID3D10EffectShaderResourceVariable.SetResourceArray
: 
---

# ID3D10EffectShaderResourceVariable::SetResourceArray


## -description


Set an array of shader resources.


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
 

 

