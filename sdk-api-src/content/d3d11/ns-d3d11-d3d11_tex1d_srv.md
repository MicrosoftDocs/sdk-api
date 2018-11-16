---
UID: NS:d3d11.D3D11_TEX1D_SRV
title: D3D11_TEX1D_SRV
author: windows-sdk-content
description: Specifies the subresource from a 1D texture to use in a shader-resource view.
old-location: direct3d11\d3d11_tex1d_srv.htm
tech.root: direct3d11
ms.assetid: 255e97ac-e978-4a70-a908-f4537337dfeb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 1bcdba84-70d7-54b7-24fa-091adf73ae90, D3D11_TEX1D_SRV, D3D11_TEX1D_SRV structure [Direct3D 11], d3d11/D3D11_TEX1D_SRV, direct3d11.d3d11_tex1d_srv
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: D3D11_TEX1D_SRV
req.redist: 
---

# D3D11_TEX1D_SRV structure


## -description


Specifies the subresource from a 1D texture to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture1D for which <a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The maximum number of mipmap levels for the view  of the texture. See the remarks.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/en-us/library/Ff476211(v=VS.85).aspx">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).

As an example, assuming <b>MostDetailedMip</b> = 6 and <b>MipLevels</b> = 2, the view will have access to 2 mipmap levels, 6 and 7, of the original texture for which <a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">ID3D11Device::CreateShaderResourceView</a> creates the view. In this situation, <b>MostDetailedMip</b> is greater than the <b>MipLevels</b> in the view. However, <b>MostDetailedMip</b> is not greater than the <b>MipLevels</b> in the original resource.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476173(v=VS.85).aspx">Resource Structures</a>
 

 

