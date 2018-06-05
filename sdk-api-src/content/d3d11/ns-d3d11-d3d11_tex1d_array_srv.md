---
UID: NS:d3d11.D3D11_TEX1D_ARRAY_SRV
title: D3D11_TEX1D_ARRAY_SRV
author: windows-sdk-content
description: Specifies the subresources from an array of 1D textures to use in a shader-resource view.
old-location: direct3d11\d3d11_tex1d_array_srv.htm
old-project: direct3d11
ms.assetid: e0caf038-d0d7-4fd4-bec3-f0023035a82a
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_TEX1D_ARRAY_SRV, D3D11_TEX1D_ARRAY_SRV structure [Direct3D 11], c31f5cd3-cca9-011f-b154-0ba95200b6e6, d3d11/D3D11_TEX1D_ARRAY_SRV, direct3d11.d3d11_tex1d_array_srv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
tech.root: 
req.typenames: D3D11_TEX1D_ARRAY_SRV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_TEX1D_ARRAY_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEX1D_ARRAY_SRV structure


## -description


Specifies the subresources from an array of 1D textures to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture1D for which <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a>.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.


### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures.


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures in the array.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

