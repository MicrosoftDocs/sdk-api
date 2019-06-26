---
UID: NS:d3d12.D3D12_TEX2D_ARRAY_SRV
title: D3D12_TEX2D_ARRAY_SRV (d3d12.h)
author: windows-sdk-content
description: Describes the subresources from an array of 2D textures to use in a shader-resource view.
old-location: direct3d12\d3d12_tex2d_array_srv.htm
tech.root: direct3d12
ms.assetid: D3854008-0BB8-4284-A89F-A13DB85BB911
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2D_ARRAY_SRV, D3D12_TEX2D_ARRAY_SRV structure, d3d12/D3D12_TEX2D_ARRAY_SRV, direct3d12.d3d12_tex2d_array_srv
ms.topic: struct
f1_keywords: 
 - "d3d12/D3D12_TEX2D_ARRAY_SRV"
req.header: d3d12.h
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
 - D3D12.h
api_name:
 - D3D12_TEX2D_ARRAY_SRV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX2D_ARRAY_SRV
req.redist: 
ms.custom: 19H1
---

# D3D12_TEX2D_ARRAY_SRV structure


## -description


Describes the subresources from an array of 2D textures to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> -1 (where <b>MipLevels</b> is from the original Texture2D for which <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview">ID3D12Device::CreateShaderResourceView</a> creates a view).
          


### -field MipLevels

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv">D3D12_TEX1D_SRV</a>.
            

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.
            


### -field FirstArraySlice

The index of the first texture to use in an array of textures.


### -field ArraySize

Number of textures in the array.


### -field PlaneSlice

The index (plane slice number) of the plane to use in an array of textures.
          


### -field ResourceMinLODClamp

A value to clamp sample LOD values to. For example, if you specify 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.


## -remarks



This structure is one member of a shader-resource-view description, <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a>.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

