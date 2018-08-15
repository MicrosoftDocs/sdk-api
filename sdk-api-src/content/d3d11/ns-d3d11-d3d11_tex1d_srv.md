---
UID: NS:d3d11.D3D11_TEX1D_SRV
title: D3D11_TEX1D_SRV
author: windows-sdk-content
description: Specifies the subresource from a 1D texture to use in a shader-resource view.
old-location: direct3d11\d3d11_tex1d_srv.htm
old-project: direct3d11
ms.assetid: 255e97ac-e978-4a70-a908-f4537337dfeb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 1bcdba84-70d7-54b7-24fa-091adf73ae90, D3D11_TEX1D_SRV, D3D11_TEX1D_SRV structure [Direct3D 11], d3d11/D3D11_TEX1D_SRV, direct3d11.d3d11_tex1d_srv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_TEX1D_SRV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX1D_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEX1D_SRV structure


## -description


Specifies the subresource from a 1D texture to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture1D for which <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum number of mipmap levels for the view  of the texture. See the remarks.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).

As an example, assuming <b>MostDetailedMip</b> = 6 and <b>MipLevels</b> = 2, the view will have access to 2 mipmap levels, 6 and 7, of the original texture for which <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a> creates the view. In this situation, <b>MostDetailedMip</b> is greater than the <b>MipLevels</b> in the view. However, <b>MostDetailedMip</b> is not greater than the <b>MipLevels</b> in the original resource.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

