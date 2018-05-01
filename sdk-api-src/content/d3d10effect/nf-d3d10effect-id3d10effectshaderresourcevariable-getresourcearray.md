---
UID: NF:d3d10effect.ID3D10EffectShaderResourceVariable.GetResourceArray
title: ID3D10EffectShaderResourceVariable::GetResourceArray method
author: windows-driver-content
description: Get an array of shader resources.
old-location: direct3d10\id3d10effectshaderresourcevariable_getresourcearray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshaderresourcevariable_getresourcearray.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetResourceArray method [Direct3D 10], GetResourceArray method [Direct3D 10], ID3D10EffectShaderResourceVariable interface, GetResourceArray,ID3D10EffectShaderResourceVariable.GetResourceArray, ID3D10EffectShaderResourceVariable, ID3D10EffectShaderResourceVariable interface [Direct3D 10], GetResourceArray method, ID3D10EffectShaderResourceVariable::GetResourceArray, be202163-a9e9-5354-d781-12b5b98cda4b, d3d10effect/ID3D10EffectShaderResourceVariable::GetResourceArray, direct3d10.id3d10effectshaderresourcevariable_getresourcearray
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
-	ID3D10EffectShaderResourceVariable.GetResourceArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectShaderResourceVariable::GetResourceArray method


## -description


Get an array of shader resources.


## -parameters




### -param ppResources [out]

Type: <b><a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">ID3D10ShaderResourceView</a>**</b>

The address of an array of shader-resource-view interfaces. See <a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">ID3D10ShaderResourceView Interface</a>.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based array index to get the first interface.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements in the array.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/636a0b4f-591a-467c-92e9-1b3d279465bb">ID3D10EffectShaderResourceVariable Interface</a>
 

 

